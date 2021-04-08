### [Princeton STEM Academy](/index.md)

## CNC Best Practices

#### Introduction

This document preserves and makes accessible the knowledge and skills that we, the Coaches, Mentors, and Team Members at the Princeton STEM Academy have gained while learning how to use our CNC machine.
It should be updated continuously.

#### Hardware and Software

We have an _Omio X8-2200L USB_.  We control it with _Mach 3_ software, running on a standard Windows 10 PC.

While our part designs come from a variety of CAD software packages (e.g, _PTC Creo Parametric_, _OnShape_), we use _AutoDesk Fusion 360_ as the CAM application.
It's how we we convert the CAD files to gcode files that can be processed by Mach 3.

#### Fusion 360 Setup

#### Adjusting for Undersized Holes

With our first few efforts, all of our holes (mounting holes, holes for shaft bearings) were undersized.
We ran a test cut in order to quantify this error, and to determine how to compensate for it at the CAD / CAM level.
Accordingly, we ran a test piece, cutting four holes, using our 3.175 mm (1/8 inch) end mill router bit.

(We're providing full detail here because this test should be repeated with router bits of various diameter.
This correction may only be valid for the 3.175 mm bit.)

Nominal diameter | Measured diameter | Error
-----------------|-------------------|-------
10 mm | 9.1 mm | 0.9 mm
20 mm | 19.25 mm | 0.75 mm
30 mm | 29.1 mm | 0.9 mm
40 mm | 39.2 mm | 0.8 mm

The error does not appear to vary with hole diameter in any systematic way.
Given the difficulties in making accurate inside measurements with precision below 0.1 mm, we're willing to assume that each hole is undersized by 0.9 mm, and will correct accordingly.

Fusion 360 has, in 2D Contouring, a _Stock to Leave_ feature.  By enabling that feature, and setting the _Radial Stock to Leave_ setting to **negative** 0.45 mm,
(radius equivalent for 0.9 mm diameter), the CAM processing will cut holes oversized from the CAD specified diameter.
When we used this process to cut 14 mm bearing holes, the bearings fit perfectly.

Again, this test should be repeated when we use other router bits, with the captured data added to this document.


#### Plan View Drawing

We **require** a _plan view drawing_ for each CNC operation.
This drawing should feature the production part(s), on the virtual raw stock, placed on the actual raw stock.
The actual raw stock should show the clamp locations (i.e., the places where the actual stock is attached to the wasteboard (sacrificial board) on the CNC).
The drawing need not be perfect, or highly detailed, but all portions should be fairly close to actual scale.

Such a drawing serves several purposes:

- It demonstrates that the pieces fit on the raw stock.
- We can assess whether or not the raw stock has enough physical integrity left to hold together as the cut progresses: both between the product and the edges of the stock, and between multiple products.
- We can determine that the router pathing clears the clamping locations by a safe margin.
- It provides guidance as to locating the origin on the raw stock.  We can find the correct corner, and determine how much clearance we need for the router path.
- It provides a reference while we're watching the "dry run" (router in the air) - that the path is what we think it is.

#### Tabs

Tabs are features added during production of the gcode in the CAM software.
They bridge the stock on either side of the router cut to preserve some structural integrity of the stock as the cut progresses.
Tabs can be cut through after the stock, containing the finished pieces, is removed from the CNC machine.

Tab size and placement is customizable in Fusion 360.
Tab height is the most critical measurement.
Tabs that are too short will disappear entirely if the stock vibrates during cutting, or if the wasteboard is not perfectly flat and level.
Tabs that are too tall will be difficult to cut out of the finished product - especially in metal.

Our experience in polycarbonate is that 1.6 mm tabs work most of the time in 6.35 mm stock, but do not survive the vibration seen when cutting 3.175 mm stock.
Paradoxically, the thinner stock needs taller tabs.
We should try 2 mm tabs for the next operation in 3.175 mm stock, and will revise this entry accordingly.

#### Materials and Bits

To date, we have only fabricated parts out of polycarbonate plastic.

**3.175 mm (1/8 inch) polycarbonate** - A very flexible material that vibrates considerably during cutting operations.
Needs disproportionately tall tabs to ensure that something is left after all that vibration.
Full height (3.175 mm) tabs are not out of the question.
We attach this to the wasteboard at four points for 12 x 12 inch raw stock, six points for 12 x 24 inch raw stock.
We're still not cutting this well.

**6.35 mm (1/4 inch) polycarbonate** - This material still cuts quickly, but stays put on the wasteboard.
Parts from this material are strong, and look good.
We attach this to the wasteboard at four points for 12 x 12 inch raw stock, six points for 12 x 24 inch raw stock.

To date, we have only used a 3.175 mm (1/8 inch) end-mill router bit.

#### Resetting the Home Position

After starting Mach 3 and powering up the CNC machine, we must establish the CNC _home_ positions (three axes).
Clicking on the _Ref All Home_ button on the Mach 3 screen will start this operation.  The CNC machine will move the router carrier in each axis until it hits the travel limit microswitch, located at maximum positive Z-axis, maximum positive Y-axis, and mimimum negative X-axis.

All actual positions are calculated relative to this _home_.
Repeat the process if you overdrive the router carriage manually, or through bad gcode.

As installed, it appears that the machine hits some mechanical X-axis limit before actuating the limit microswitch.
We fixed that by gluing a small piece of particle board to the router carriage to ensure that the carriage closes the microswitch before the motor overdrives the mechanism.

#### Setting the Origin: X and Y Axes

#### The "Dry Run": Cutting in the Air

#### Zeroing the Z Axis

The final step before cutting your stock is to set the height of the router bit - the Z axis "zero" point - just touching the raw stock.

Setting the Z-axis "zero" location exactly right is critical to getting a good cut.
Too high, and you won't cut through all of your stock.  Too low, and you'll gouge into the wasteboard, and may lose the tabs from your cutting path -
which might cause your cut to fail or produce dangerous shifting of your stock.

You **must** be familiar with the manual motion controls: both the controls on the Mach 3 dashboard (MPG window), and on the hand-held remote control.

Both allow you to move the router carriage continously, by holding down the control button.
Both allow you to select a 1.0 mm step, where each button press moves the carriage by 1 mm, up or down.
Both allow you to select a 0.1 mm step, where each button press moves the carriage by 0.1 mm, up or down.
The Mach 3 control dashboard also allows several smaller steps.  We have not yet found it necessary to use them.

Your goal is to bring the tip of the router bit in contact with the raw stock, but not exerting any pressure on it.
We use the thickness of a piece of paper as our test gauge: we want a single 0.1 mm change to make the difference between being able to slide the paper under the router bit,
and the paper being blocked by the bit.
Then, we set the Z-axis zero on Mach 3.

Step-by-step process:

- If your wasteboard is not perfectly planar with the X - Y motion of the carriage, move the carriage roughly to the mid-point between the high side and the low side.

- By eye, move the router bit close to the raw stock.  Use the continuous motion setting on the remote control, or on the Mach 3 dashboard.

- Switch to the 1 mm step function on either control.  Continue approaching the raw stock.
When you get close enough, use the paper test to ensure that the bit is not yet touching the stock.

- When you can no longer pass the paper between the bit and the stock, bring the bit back up by one step (1 mm).

- Change the step setting to 0.1 mm.

- Again, bring the bit closer to the stock, one step (0.1 mnm) at a time, checking with the paper each time. 
Stop after the bit first touches the stock and you can no longer slide the paper under the bit.

- Set the Z axis "zero" on the Mach 3 dashboard.

- **Move the router carriage up several inches** before attempting to move the carriage in the X or Y axes.
(You do not have to return the router to your X - Y zero location to start your cut.
Most likely, you can leave the router right where it is.)


[_home / index_](/index.md)

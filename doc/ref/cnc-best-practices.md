### Princeton STEM Academy

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

3.175 mm (1/8 inch) polycarbonate - A very flexible material that vibrates considerably during cutting operations.
Needs disproportionately tall tabs to ensure that something is left after all that vibration.
Full height (3.175 mm) tabs are not out of the question.
We attach this to the wasteboard at four points for 12 x 12 inch raw stock, six points for 12 x 24 inch raw stock.
We're still not cutting this well.

6.35 mm (1/4 inch) polycarbonate - This material still cuts quickly, but stays put on the wasteboard.
Parts from this material are strong, and look good.
We attach this to the wasteboard at four points for 12 x 12 inch raw stock, six points for 12 x 24 inch raw stock.

To date, we have only used a 3.175 mm (1/8 inch) end-mill router bit.

#### Resetting the Home Position

#### Setting the Origin: X and Y Axes

#### The "Dry Run": Cutting in the Air

#### Zeroing the Z Axis

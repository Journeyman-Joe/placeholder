## CNC Best Practices

### Princeton STEM Academy

#### Plan View Drawing

We **require** a _plan view drawing_ for each CNC operation.
This drawing should feature the production part(s), on the virtual raw stock, placed on the actual raw stock.
The actual raw stock should show the clamp locations (i.e., the places where the actual stock is attached to the sacrificial board on the CNC).
The drawing need not be perfect, or highly detailed, but all portions should be fairly close to actual scale.

Such a drawing serves several purposes:

1. It demonstrates that the pieces fit on the raw stock.
2. We can assess whether or not the raw stock has enough physical integrity left to hold together as the cut progresses: both between the product and the edges of the stock, and between multiple products.
3. We can determine that the router pathing clears the clamping locations by a safe margin.
4. It provides guidance as to locating the origin on the raw stock.  We can find the correct corner, and determine how much clearance we need for the router path.
5. It provides a reference while we're watching the "dry run" (router in the air) - that the path is what we think it is.

#### Tabs

Tabs are features added during production of the gcode in the CAM software.
They bridge the stock on either side of the router cut to preserve some structural integrity of the stock as the cut progresses.
Tabs can be cut through after the stock, containing the finished pieces, is removed from the CNC machine.



Even at reduced feed speed, we get a lot of stock vibration with 1/8 inch (3.175 mm) plastic.  The tabs have to be taller, perhaps even full height, in order to work properly.

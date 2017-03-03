# Developer guide: How to create mobile-friendly custom visual
One of Power BI's major strengths is staying connected to your data from anywhere, anytime, with the Power BI app for Windows, iOS, and Android. Business users can get a 360° view of your business data on the go - at the touch of their fingertips.  
Mobile consumption plays a major role in Power BI, and creating custom visuals that address the unique needs of mobile devices should be one of your top of minds as a developer, to reach as many user as possible and provide them with the best experience possible.

## Must-Have requirements
The following requirements are essential in development of mobile-friendly visual.

### Rendering
Custom visual must render on all supported mobile browsers and mobile applications without errors in reports, dashboards and in focus mode. 

### Interactivity
Interactivity is important in order to provide the same functionality as for desktop devices. Try to support all events that are handled on desktop browsers or support analogous event handlers for mobile devices. Selection of data points and navigation should be implemented if visual provides such functionality on desktop browsers. If visual supports multi-selecting using Ctrl key - consider adding similar event handling for mobile devices.

Note that mobile devices (touch screen devices) don't support any mouse events (all events with "mouse" prefix). In other words, you have to listen to mouse and touch events at the same.

Use the following table in order to choose the correct event name at mobile devices:

| Mouse event name | Touch event name |
|:----------------:|:----------------:|
| click | click |
| mousemove | touchmove |
| mousedown | touchstart |
| mouseup | touchend |
| dblclick | Use external library |
| contextmenu | Use external library |
| mouseover | touchmove |
| mouseout | touchmove (external library) |
| wheel | NaN |

## Nice-to-Have requirements
Consider implementing requirements below to provide the best experience for mobile users.

###Rendering
Support small sizes of the visual. Visual should be mobile-friendly in Focus mode – it should be optimized for the mobile screen size and support both portrait and landscape orientations. Add new formatting options to change the size of visual elements (for example, of labels). Such improvement will allow users to customize visual for their dashboards on mobile devices.

### Failover
Visual should show descriptive error if it cannot be rendered on mobile devices for some reasons.

### Interactions
Consider adding mobile-specific event handlers, like dragging.

## Supported browsers and devices
Visual should be rendered on all devices that support Power BI Apps - see details [here](https://powerbi.microsoft.com/en-us/documentation/powerbi-power-bi-apps-for-mobile-devices/). Also test your visual in default browsers for Windows 10, iOS and Android devices.

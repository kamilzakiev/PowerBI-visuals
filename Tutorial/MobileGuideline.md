# Developer guide: How to create mobile-friendly custom visual
Power BI allows to stay connected to your data everywhere and offers everyone mobile support of Power BI reports and dashboards as long as Power BI apps for Windows, iOS, and Android devices. Many Power BI users are using mobile devices, so development of mobile-friendly experience should be important part of your visual development.

## Must-Have requirements
The following requirements are essential in development of mobile-friendly visual.

### Rendering
Custom visual should render on all supported mobile browsers and mobile applications without errors in reports, dashboards and in focus mode. 

### Performance
Visual should take less than 10 seconds to render using sample data.

### Interactivity
Interactivity is important in order to provide the same functionality as for desktop devices. Try to support all events that are handled on desktop browsers or support analogous event handlers for mobile devices. Selection of data points and navigation should be implemented if visual provides such functionality in desktop browsers. If visual supports multi-selecting using Ctrl key - consider adding similar event handling for mobile devices.

Please consider that mobile devices (touch screen devices) don't support any mouse events (all events with "mouse" prefix). In other words, you have to listen to mouse and touch events at the same.

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

### Performance
It is good to have the same performance of the visual on mobile as in desktop browsers.

### Failover
Visual should show desriptive error if it cannot be rendered on mobile devices for some reasons.

### Interactions
Consider adding mobile-specific event handlers, like dragging.

## Supported browsers and devices
Visual should be rendered on all devices that support Power BI Apps - see details [here](https://powerbi.microsoft.com/en-us/documentation/powerbi-power-bi-apps-for-mobile-devices/). Also test your visual in default browsers for Windows 10, iOS and Android devices.

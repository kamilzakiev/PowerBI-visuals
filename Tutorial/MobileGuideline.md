# Developer guide: How to create mobile-friendly custom visual
Power BI allows to stay connected to your data everywhere and offers everyone mobile support of Power BI reports and dashboards as long as Power BI apps for Windows, iOS, and Android devices. Many Power BI users are using mobile devices, so development of mobile-friendly experience should be important part of your visual development.

## Must-Have requirements
### Rendering
Custom vis will render on mobile (meaning, it will not fail)
Will render in focus mode, in reports in dashboards

### Performance
Render time - 10 sec

### Interactions
Select data points
Navigate

## Nice-to-Have requirements

###Rendering
Focus mode for mobile will be mobile friendly – optimized for the mobile screen size/portrait and landscape
Support small sizes of the visual
Formatting options to change the size of visual elements (labels for example)

### Performance
// Custom visuals should be fast at mobile devices, because mobile devices aren't so fast as PC http://bl.ocks.org/mbostock/3808218 - D3's update pattern https://github.com/d3/d3-selection/blob/master/README.md#joining-data - D3 joining data

// We might reduce amount of data at mobile device in order to improve performance.

### Failover
Nice message when error

### Interactions
Dragging/Drill down

## Supported devices


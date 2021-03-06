# <a name="top"></a>Sensor Visualizers
When in a non-Headless Simulation, sensor visualizers can be toggled from the menu. To visualize a sensor, click the "eye" next to the sensor name.

[![](images/visualizer-menu.png)](images/full_size_images/visualizer-menu.png)

Sensors are identified by the `name` parameter from the JSON configuration. 
For full details on the possible JSON parameters see [Sensor Parameters](sensor-json-options.md)
Not all sensors have visualizations available, only sensors who have will show their visualizations.

<h2>Table of Contents</h2>
[TOC]

## Transform Visualization [[top]] {: #transform-visualization data-toc-label='Transform Visualization'}

For each sensor, you can click the "coordinate" icon next to the sensor name to turn on the visualization of the sensor's transform. This transform is shown relative to the parent [transform sensor](sensor-json-options.md#transform-sensor), if present (base_link).

<div class="video-container">
    <iframe style="display:block;margin:auto;" width="696" height="391" src="https://www.youtube.com/embed/Q00B7vqtwrE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<br>

## Cameras [[top]] {: #cameras data-toc-label='Cameras'}

When a camera is visualized, the image the sensor see is visualized in a window. 
This window can be resized by clicking-and-dragging the icon in the bottom right corner and can be made full-screen with the box icon in the top right corner. 
The window can be moved by clicking-and-dragging the top bar. To close the window, either click the `X` or click the "eye" again.

### Color Camera [[top]] {: #color-camera data-toc-label='Color Camera'}
Visualized Color camera shows the same things that are visible from the normal follow and free cameras, but from the perpsective defined in the JSON configuration.

[![](images/color-camera-visualized.png)](images/full_size_images/color-camera-visualized.png)

### Depth Camera [[top]] {: #depth-camera data-toc-label='Depth Camera'}
Visualized Depth camera shows objects colored on a grayscale based on the distance between the camera and the object.

[![](images/depth-camera-visualized.png)](images/full_size_images/depth-camera-visualized.png)

### Segmentation Camera [[top]] {: #segmentation-camera data-toc-label='Segmentation Camera'}
Visualized Segmentation camera shows objects colored according to the object tag.

|Tag|Color|Hex Value|
|:-:|:-:|:-:|
|Car|Blue|#120E97|
|Road|Purple|#7A3F83|
|Sidewalk|Orange|#BA8350|
|Vegetation|Green|#71C02F|
|Obstacle|White|#FFFFFF|
|TrafficLight|Yellow|#FFFF00|
|Building|Turquoise|#238688|
|Sign|Dark Yellow|#C0C000|
|Shoulder|Pink|#FF00FF|
|Pedestrian|Red|#FF0000|
|Curb|Dark Purple|#4A254F|

If a tag is included in "InstanceSegmentationTags", each instance of objects with that tag is colored differently, but all will have same hue. For example, the following figure shows a segmentation result with semantic "Car" having instance segmentation (note that cars are all bluish but each instance has a different color).

[![](images/segmentation-visualized.png)](images/full_size_images/segmentation-visualized.png)

### 2D Ground Truth [[top]] {: #2d-ground-truth data-toc-label='2D Ground Truth'}
Visualized 2D Ground Truth shows the same things as a color camera except pedestrians are enclosed in a yellow wire box and NPCs are enclosed in a green wire box.

[![](images/2d-ground-truth-visualized.png)](images/full_size_images/2d-ground-truth-visualized.png)

## Lidar [[top]] {: #lidar data-toc-label='Lidar'}
Visualized Lidar shows the point cloud that is detected.

[![](images/lidar-visualized.png)](images/full_size_images/lidar-visualized.png)

## Radar [[top]] {: #radar data-toc-label='Radar'}
Visualized Radar shows the radar cones and creates wireframe boxes enclosing NPCs ni a green box, bicycles in a cyan box, and other EGOs in a magenta box.

[![](images/radar-visualized.png)](images/full_size_images/radar-visualized.png)

## 3D Ground Truth [[top]] {: #3d-ground-truth data-toc-label='3D Ground Truth'}
Visualized 3D Ground Truth creates wireframe boxes enclosing pedestrians in a yellow box and NPCs in a green box.

[![](images/visualizer-menu.png)](images/full_size_images/visualizer-menu.png)

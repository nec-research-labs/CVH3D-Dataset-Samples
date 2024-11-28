# CVH3D-Dataset-Samples
Sample triplets of Ground Image, Aerial Image and 3D Point Cloud from CVH3D dataset

|:--:|:--:|:--:|
| Ground View Image | Aerial View Image | 3D Point Cloud |
|<img src="/CVH3D/111050484379850/111050484379850.jpg" alt="drawing" height="100"/> |<img src="/CVH3D/111050484379850/111050484379850_sat.jpg" alt="drawing" width="100"/> |<img src="/CVH3D/111050484379850/111050484379850_3D.png" alt="drawing" height="100"/> |


This repository contains samples from our dataset CVH3D containing Ground-view, Aerial-view and 3D Point Cloud<br>
- All Ground-view images were downloaded from Mapillary using their API<br>
- Aerial images were downloaded from the database of National Land Survey of Finland. The resolution of the aerial images is 50 cm.<br>
- 3D Mesh samples were downloaded from Helsinki City Municipality website.<br>
- All the above data has been released to public. The data samples shared are licensed under their respective publishers.<br>

Ground Image Source:<br>
Mapillary: https://www.mapillary.com<br>
(licensed under CC-BY-SA)<br>
 
Aerial Image Source:<br>
National Land Survey of Finland<br>
https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/datasets-and-interfaces/product-descriptions/orthophotos<br>
(licensed under CC-BY-4.0)<br>
 
3d Data Source:<br>
Helsinki City Municipality (City of Helsinki)<br>
https://www.hel.fi/en/decision-making/information-on-helsinki/maps-and-geospatial-data/helsinki-3d<br>
(licensed under CC-BY-4.0)<br>


## Visualizing 3D Point Cloud:
	- 3D Point Cloud samples are saved in .pcd format
	- To visualize the point cloud samples please follow below steps
	1. Install Open3D library (https://pypi.org/project/open3d/):
		- pip install open3d
	2. Use below python code to visualize point cloud:
 
```markdown
import open3d as o3d
pcd = o3d.io.read_point_cloud(pcd_path)  # replace 'pcd_path' with path to the pcd sample
o3d.visualization.draw_geometries([pcd])
```

NOTE: Aerial images were cropped in 200m x 200m squares and 3D Point Cloud samples were cropped in 100m x 100m cubes. Details are mentioned in the paper.

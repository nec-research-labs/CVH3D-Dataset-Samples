# CVH3D-Dataset-Samples
Sample triplets of Ground Image, Aerial Image and 3D Point Cloud from CVH3D dataset

This zip file contains samples from our dataset containing Ground-view, Aerial-view and 3D Point Cloud
	- All Ground-view images were downloaded from Mapillary using their API
	- Aerial images were downloaded from the database of National Land Survey of Finland. The resolution of the aerial images is 50 cm.
	- 3D Mesh samples were downloaded from Helsinki City Municipality website.
	- All the above data has been released to public. The data samples shared are licensed under their respective publishers.

Ground Image Source:
Mapillary: https://www.mapillary.com
(licensed under CC-BY-SA)
 
Aerial Image Source:
National Land Survey of Finland
https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/datasets-and-interfaces/product-descriptions/orthophotos
(licensed under CC-BY-4.0)
 
3d Data Source:
Helsinki City Municipality
https://www.hel.fi/en/decision-making/information-on-helsinki/maps-and-geospatial-data/helsinki-3d
(licensed under CC-BY-4.0)


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

NOTE: All the Aerial and 3D Point Cloud samples are cropped in 100m x 100m squares (cubes for point cloud)

# cemba_dissection

This repository contains CEMBA dissction region segmentation based on Allen CCFv3 and its average template at 25 micron resolution. This repo provides content to [the CEMBA snmC-seq2 data browser](http://neomorph.salk.edu/omb)

## Allen CCFv3
- See documentation about Allen CCFv3 from the AIBS: https://community.brain-map.org/t/allen-mouse-ccf-accessing-and-using-related-data-and-tools/359
- To view the dissection segmentation, you need to first unzip the Allen CCFv3 files. All the files downloaded from Allen brain atlas from [here](http://download.alleninstitute.org/publications/allen_mouse_brain_common_coordinate_framework/transgenic_lines_25_um_grid/ccf/), and this paper: Wang, Quanxin, Song-Lin Ding, Yang Li, Josh Royall, David Feng, Phil Lesnar, Nile Graddis, et al. 2020. “The Allen Mouse Brain Common Coordinate Framework: A 3D Reference Atlas.” Cell 181 (4): 936–53.e20.
- Average template NRRD is the background of the segmentation
- The annotation NRRD is the CCFv3 brain structure segmentation
- The txt file contain color and label of CCFv3 structures that can be loaded into ITK-SNAP
- There is a nice documentation in the Allen CCFv3 files (`ITK-SNAP_SOP for viewing Tg data and average template.docx`) about how to view the CCFv3 files in ITK-SNAP.

## ITK-SNAP
Install latest ITK-SNAP to view NRRD files.
http://www.itksnap.org/pmwiki/pmwiki.php

## CEMBA Dissection Segmentation
- Both `CEMBA_region.nii.gz` and `CEMBA_region.nrrd.gz` are the dissection region segmentations on the CCF's average template.
- `CEMBA_region_anno_itksnap.txt` contain color and label of CEMBA dissection regions.
- As explained in the documentation from Allen CCF (`ITK-SNAP_SOP for viewing Tg data and average template.docx`), load the average template and CEMBA dissection segmentation in ITK-SNAP to view it or generate mesh.

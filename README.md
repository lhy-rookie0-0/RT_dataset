# RT Dataset — Urban street-tree detection

The RT dataset contains 2,313 JPEG images and matching YOLO bounding-box annotations for eight street-tree classes. This package contains 1,850 training, 235 validation, and 228 test images. The split is stratified by annotation class and shuffled with seed 20261105. It is a new split and should not be assumed to reproduce scores obtained with a different split.

## Download and extraction

Download all RT_dataset_*.zip files from the release. Each ZIP is a standalone archive, not a volume of a larger archive. Extract each ZIP into the same directory, keeping the paths inside the ZIP. The expected structure is:

    images/train/  images/val/  images/test/
    labels/train/  labels/val/  labels/test/

The release checksum file lists SHA-256 digests for all archives. The split manifest records image and label paths and their subset assignments. There should be one matching TXT file per JPEG. Each nonblank label row is: class_id x_center y_center width height. Box coordinates are normalized to the image dimensions; class IDs start at zero.

| ID | Class name in manuscript |
|---:|---|
| 0 | Cinnamomum camphora |
| 1 | Ligustrum lucidum |
| 2 | Magnolia grandiflora |
| 3 | Osmanthus fragrans |
| 4 | Lagerstroemia indica |
| 5 | Juniperus chinensis 'Pyramidalis' |
| 6 | Pyrus pyrifolia |
| 7 | Sophora japonica |

Some original filenames retain historical class names. The numeric labels determine class membership.

Release: https://github.com/lhy-rookie0-0/RT_dataset/releases/tag/rt-dataset-20261105

The repository also provides data.yaml for YOLO and split_manifest.csv for the exact image and label assignments. Set the dataset root to the directory into which all archives were extracted.

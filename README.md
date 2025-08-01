# (ICCV 25)MonoFusion: Sparse-View 4D Reconstruction via Monocular Fusion
**[Project Page](https://imnotprepared.github.io/research/25_DSR/) | [Arxiv]() | [Data](https://drive.google.com/drive/folders/18H8OOOZLv7OmOen8pGbSLWwu8AvZAZro?usp=sharing)**

[Zihan Wang](https://imnotprepared.github.io/), [Jeff Tan](https://jefftan969.github.io/), [Tarasha Khurana](https://www.cs.cmu.edu/~tkhurana/)\*, [Neehar Peri](https://www.neeharperi.com)\*, [Deva Ramanan](https://www.cs.cmu.edu/~deva/)

Carnegie Mellon University

\* Equal Contribution



## Installation

```
git clone --recurse-submodules https://github.com/ImNotPrepared/MonoFusion
cd MonoFusion/
conda create -n monofusion python=3.10
conda activate monofusion
```

Update `requirements.txt` with correct CUDA version for PyTorch and cuUML, 
i.e., replacing `cu122` and `cu12` with your CUDA version. 
```

pip install -r requirements.txt
pip install git+https://github.com/nerfstudio-project/gsplat.git
```

## Todo List

| Task | Status | Due Date |
|------|--------|----------|
| Complete installation guide | ✅ Done | - |
| Preprocessing scripts | ⏳ Todo | in a week |
| Drop Code | ⏳ Todo | between ICLR and ICCV |

## Usage
Yes we know processing data is a headache, that is why we've got you covered. One button press gets you undistorted, synchronized sparse-view data with all the priors you need.

### Get Ego-Exo4D Access

To work with Ego-Exo4D data, follow these steps:

1. **Obtain License**: Get a license for Ego-Exo4D at https://docs.ego-exo4d-data.org/getting-started/

2. **Download VRS Files**: Download VRS files with RGB stream for a specific take:
   ```
   egoexo -o <output_directory> --parts take_vrs --uids <uid1>
   ```
   Note: VRS files are required to ensure synchronized data streams.

3. **Extract Images**: Extract undistorted images from the VRS sequences:
   ```
   viewer_map --vrs aria01.vrs --task vis --resize 512
   ```
   The default resize resolution is 512 pixels


### Preprocessing
We have one-button-push priors generation script that saves depth maps, human masks, dino feature, and 2D tracks.

```
./fetch_priors.sh
```



### Start your own EgoRecon (⏳)



## Citation
```
```
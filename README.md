# 3DRadioMap_Dataset
## A 3D air-to-ground radio map dataset

This dataset is generated using a commercial ray tracing (RT) software, _Remcom Wireless Insite_ (WI), with a maximum of 6 reflections and 3 diffractions. Simulation environment is based on an urban area of Nanjing Road in Shanghai, China. The region of interest is a square area of side 650 meters and the aerial transmitters (TXs) are randomly distributed with altitudes ranging from 50 to 200 meters. The heights of the ground receivers (RXs) are fixed at 2 meters. The waveform is chosen as sinusoidal signal at 5.9 GHz with 10MHz bandwidth and there is 3 dB noise to the receivers.

## Document：
**Shanghai_Dproj**: The simulation project of WI.

**radiomap_raw**: The raw simulation output files generated by WI. The number in filenames "A50"~"A100" represent the simulated emulation heights of transmitters in different settings.

**radiomap_processed**: The processed channel path loss data is saved in MAT format, following the same filename conventions as the original data. The storage format is (RX_coordinates, TX_coordinates, Distance, Path loss, null).

**radiomap_shanghai100tx_2.5GHz.mat; radiomap_shanghai115tx_28GHz.mat**：This two datasets are simulated at 2.5GHz and 28GHz, respectively.

## City Map and 3D terrain

The city map of an urban area of Nanjing Road in Shanghai and the corresponding 3D terrain of the city map in the Simulation.

<img src="https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/CityMap.jpg" width="500px">

![The terrain map of an urban area of Nanjing Road in Shanghai.](https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/CityMap.jpg)
![The 3D terrain of the city map.](https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/3DMap.jpg)

## An example of RT result

For a typical fixed TX-RX position pair, a RT result is presented to demonstrate multiple reflections and diffractions. The RT result shows the signal paths between the TX and RX, including several reflections off walls and diffractions around corners.

![RT](https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/Multipath.jpg)

## Several slices of the generated radio map.

A 2D slice of the path loss radio map for a fixed TX position.

![The path loss map for a fixed TX position.](https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/RadioMap1.png) ![The path loss map for a fixed TX position.](https://github.com/chenwangqian-dr/3DRadioMap_Dataset/blob/main/figures/RadioMap2.png)

## Reference

For the 3D air-to-ground radio map dataset, please cite the following papers：

W. Chen, and J. Chen, “Diffraction and Scattering Aware Radio Map and Environment Reconstruction using Geometry Model-Assisted Deep Learning”, arXiv:2403.00229, 2024.

W. Chen, and J. Chen, "Blockage-aware Radio Map Construction via Exploiting the Diffraction and Obstruction Structure", in Proc. IEEE Glob. Commun. Conf. (GLOBECOM), 2023, pp. 1920-1925.

W. Liu and J. Chen, “UAV-aided radio map construction exploiting environment semantics”, IEEE Trans. on Wireless Commun., vol. 22, no. 9, pp. 6341–6355, 2023.


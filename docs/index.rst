.. MUN-FRL Dataset documentation master file, created by
   sphinx-quickstart on Sat Oct 15 14:42:58 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

MUN-FRL: Aerial Visual-Inertial-LiDAR Odometry and Mapping Dataset 
===================================================================

.. image:: /images/pl1.jpg
   :width: 23%
.. image:: /images/pl_v1.png
   :width: 35%
.. image:: /images/LH_m600_flight_cp.png
   :width: 39%
.. image:: /images/bell_1_map.jpg
   :width: 98%
   
This webpage presents the visual-inertial-LiDAR (VIL) datasets collected by an interchagable payload unit atttached to 
a Bell 412 Advanced Systems Research Helicopter (ASRA) helicoptor and a DJI M600 hexacoptor drone.
The payload unit consists of two monocular/RGB global shutter cameras, a 3D LiDAR, an IMU, real-time kinematic (RTK) enabled 
global navigation system (GNSS) receiver and a Jetson AGX Xavier GPU as the processing unit.
The two cameras, IMU, LiDAR and GNSS receivers are hardware time-synchronized.

Latest Updates
--------------

* **[March 2026]** **New Calibration Data:** Added comprehensive intrinsic and extrinsic calibration datasets for the Bell 412 platform. See the :doc:`Calibration` page.
* **[March 2026]** **License Update:** The dataset files are now explicitly licensed under **CC BY 4.0** to facilitate both academic and commercial use. See :ref:`license-section`.

Available Data
--------------
Images
++++++
* FLIR BFS-U3-16S2M-BD - Nadir view [global shutter, 1140x1080, monochrome (Mono8) and color (RGB8), 20Hz]
* FLIR BFS-PGE-04S2C-CS - Forward view [global shutter, 720x540, monochrome (Mono8) and color (RGB8), 20Hz]
  
IMU Measurements
++++++++++++++++
* Xsens MTi-30 IMU - [angular rate, accleration - 400Hz, magnetic field - 100Hz]

Pointclouds
+++++++++++
* Velodyne VLP-16 LiDAR - Downward facing [pointclouds, 360° horizontal, 30° vertical FOV, 10Hz] 

Ground-Truth
++++++++++++
* simpleRTK2B RTK-GNSS receriver - [3D position, 5Hz]
* Post processed kenematic (PPK) ground truth - [3D position, 5Hz]



Downloads 
---------
.. csv-table:: 
   :header: Dataset,Size [GB],Length [m],Duration [s],ROS bag, PPK file, FRL file
   :widths: 20,10,10,10,10,10,10
   
   quarry1,27.2,357,231, `link <https://drive.google.com/drive/folders/1-cN8PKBhh5REuKsP69V0s5cf-PcBO_eR?usp=sharing>`_ , `link <https://drive.google.com/file/d/1_o1gtOxE9OKpIxHf8rQa-njHIaFDRnmz/view?usp=drive_link>`_ , N/A
   quarry2,79.8,807,675, `link <https://drive.google.com/drive/folders/1flDXDGoUXpRpQisJcKXBH-tTqEwC6UZg?usp=sharing>`_ , `link <https://drive.google.com/file/d/1OH3xXRmlJZkQfkF8ayqkwyFddo-FJcTm/view?usp=drive_link>`_ , N/A
   lighthouse,89.9,890,756, `link <https://drive.google.com/drive/folders/1TzMhbG5N4v6L8JeI1XPaw9YCpwuj8jbI?usp=sharing>`_ , `link <https://drive.google.com/file/d/1G88Zn8D89oLvV_ExBxOtbgLTpJT9zU6x/view?usp=drive_link>`_ , N/A 
   bell412_dataset1,45.9,1709,432, `link <https://drive.google.com/drive/folders/18jG0_auUzMB6SNq_xTYDs2vzMYAebGIc?usp=sharing>`_ , `link <https://drive.google.com/file/d/1zK2UMIZUWkcNl0k01pwq4I5xa0vSvGYW/view?usp=drive_link>`_ , `link <https://drive.google.com/file/d/14blQp61TXsJWpynAyUqd5QwHjYCvMp7I/view?usp=drive_link>`_
   bell412_dataset2,45.8,x,436, `link <https://drive.google.com/drive/folders/1gql9_Wydn7Kyc7hC6V8BFugDDbYJgsTt?usp=sharing>`_ , `link <https://drive.google.com/file/d/1It0Qbp2U7jPTEbw4pYyzgnkAo1JnMZ5s/view?usp=drive_link>`_ , `link <https://drive.google.com/file/d/13wTOElgrKPxdtf6M2SJ_nuP_8A7kv6iH/view?usp=drive_link>`_
   bell412_dataset3,32.2,4336,308, `link <https://drive.google.com/drive/folders/1CbSIJEn9XPw4c0HJrn3_gIDifTR6rhLx?usp=sharing>`_ , `link <https://drive.google.com/file/d/1GvOMj341y_dITWkWXnQi7lQ5o4YzpCzm/view?usp=drive_link>`_ , `link <https://drive.google.com/file/d/1EGQTdouR1ZCMWMFeye4szolx5tFaW4ql/view?usp=drive_link>`_
   bell412_dataset4,33.0,3656,316, `link <https://drive.google.com/drive/folders/1MjBBT7bxMADMQE5r0wTlVj4p17yT6Gjg?usp=sharing>`_ , `link <https://drive.google.com/file/d/1bUc83cJ5DeQRI09DOQLwUi4vnFNp1hUv/view?usp=drive_link>`_ , `link <https://drive.google.com/file/d/1nnZqsSc12RyQp6HlzIjOQLzxXyVsAeHm/view?usp=drive_link>`_
   bell412_dataset5,34.1,2138,483, `link <https://drive.google.com/drive/folders/1tBHKwTXkFQTpK57eI5ySmqV6iw8SHFg5?usp=sharing>`_ , `link <https://drive.google.com/file/d/1UE4eAAWE71MqgqdFbR0fWDRxuNlMCL5w/view?usp=drive_link>`_ , `link <https://drive.google.com/file/d/1vMNRDUTxcJz-5e49FwJB5ij-kuFfYU_Z/view?usp=drive_link>`_
   bell412_dataset6,47.6,4938,520, `link <https://drive.google.com/drive/folders/1FONJtovVx__3iLLVI_ET8yheDF9-ZWqG?usp=sharing>`_ , `WIP <link>`_ , `link <https://drive.google.com/file/d/1sE5cfKJ4DHxjXvHAxtj_M34b6Zjso1GW/view?usp=drive_link>`_

Quick Tests on State-of-the-art Algorithms
------------------------------------------
.. csv-table:: 
   :header: Algorithm, Git repo with munfrl launch files
   :widths: 10,30

   VINS-Fusion , https://github.com/sendtooscar/VINS-Fusion-gpu
   FAST-LIO2 , https://github.com/sendtooscar/FAST_LIO.git
   ALOAM , https://github.com/sendtooscar/A-LOAM
   SVO2 ,  https://github.com/sendtooscar/SVO2 
   FAST-LVIO2 , work-in-progres

CCECE 2025 Workshop Material
------------------------------------------
.. csv-table:: 
   :header: Type, Description, Size, Download Link
   :widths: 10,30,10,10

   Data bag,Bell412_dataset1_benchmarking_bag, 6.00 GB, `link <https://drive.google.com/file/d/1dxZcWZ_J7QEXkDjaHdePMfO5him3EZuf/view>`_
   Data bag, Lighthouse_benchmarking_bag, 3.55 GB, `link <https://drive.google.com/file/d/15MovyJSUhj0D2cgWNklvQTru7j6JfUwb/view>`_
   Foxglove layout,  Fox glove raw data visualization layout, 5 KB, `link <https://drive.google.com/file/d/1h3DzfUo1ufb4LfpoL19HUjXpHZuWray0/view>`_
   Foxglove layout,  Fox glove processed data visualization layout, 15 KB, `link <https://drive.google.com/file/d/19L6q4tPR29Cot9sCYrmtOkYf3Ro_E6f8/view>`_
   Colab Notebook, Landing zone tutorial notebook link (Google Colab), online, `link <https://drive.google.com/file/d/10qk9eo0EzPJp9uYMYXzeYj8xzNVGNQD9/view>`_
   Colab Notebook, Radar Super resolution tutorial notebook link (Google Colab), online, `link <https://drive.google.com/file/d/1rFruABddIvH_jon4MNT2riCC1w3PU-89/view>`_
   Colab Notebook, GCS trajectory optimization tutorial notebook link (Google Colab), online, `link <https://colab.research.google.com/drive/14dXIk6KSdbuP5h3W5uuXNHsDg7ZttbBx?usp=sharing>`_



Lisence
-------
The **MUN-FRL Dataset** (including all LiDAR pointclouds, GPS/IMU logs, and RGB images) is licensed under a `Creative Commons Attribution 4.0 International (CC BY 4.0) <https://creativecommons.org/licenses/by/4.0/>`_ License. 

.. note::
   While the IJRR publication is distributed under a Non-Commercial (CC BY-NC 4.0) license, the **underlying raw data and calibration files provided here are explicitly licensed under CC BY 4.0** to support both academic and commercial research in aerial autonomy.

Under this license, you are free to:
* **Share** — copy and redistribute the material in any medium or format.
* **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.

**The only requirement is that you give appropriate credit by citing the original paper.**

Citation
--------

If you use this dataset or the associated tools in your research, please cite the following publication:

.. code-block:: bibtex

   @article{thalagala2024munfrl,
     title={MUN-FRL: A Visual-Inertial-LiDAR Dataset for Aerial Autonomous Navigation and Mapping},
     author={Thalagala, Ravindu G and De Silva, Oscar, Mann, George KI and Gosine, Raymond G},
     journal={The International Journal of Robotics Research},
     volume={43},
     number={12},
     pages={1853--1866},
     year={2024},
     publisher={SAGE Publications},
     doi={10.1177/02783649241238318}
   }

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Dataset Overview

   sensors
   Calibration
   ground truth

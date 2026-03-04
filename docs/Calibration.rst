Sensor Calibration
==================
To assist in explaining the calibration process presented in this section, 
the hardware measurements and schematic of the coordinate system transformations are provided below.

.. image:: /images/side_ann.svg
   :width: 50%
.. image:: /images/tf.svg
   :width: 49%

Calibration datasets
----------------------------
The following datasets provide the raw data used to compute the extrinsic and intrinsic parameters for the Bell 412 seqences.

.. list-table:: 
   :widths: 30 70
   :header-rows: 1

   * - Dataset Type
     - Download Link
   * - **Down-facing Camera** (Intrinsics)
     - `Google Drive Folder <https://drive.google.com/drive/folders/1pJNCq15vsOUnff5wMYKAWgCjiDaWDqXM?usp=sharing>`_
   * - **Front-facing Camera** (Intrinsics)
     - `Google Drive Folder <https://drive.google.com/drive/folders/1IoHBQ5MUdzUzwFNntslbvHv_K3IwuYDW?usp=sharing>`_
   * - **IMU + Down-facing Camera** (Extrinsics)
     - `Download File <https://drive.google.com/file/d/1nOH9lzuz5oSh4aGuZv6TUw7zf-_mTwz2/view?usp=sharing>`_
   * - **IMU + Front-facing Camera** (Extrinsics)
     - `Download File <https://drive.google.com/file/d/1mIOt4IDnGuwTuVgKvmhKzxwGah5ReIVd/view?usp=sharing>`_
   * - **LiDAR + Down-facing Camera** (Extrinsics)
     - `Google Drive Folder <https://drive.google.com/drive/folders/1xUG8HLlKMLoxFRPjKxE4I-vI1O6d-MZI?usp=sharing>`_
   * - **LiDAR + Front-facing Camera** (Extrinsics)
     - `Google Drive Folder <https://drive.google.com/drive/folders/1vA1zss1RAvS3YwoSqxbQJbaLUDk7Wgx_?usp=sharing>`_

.. note::
   Calibration data for DJI M600 sequences are not available.

Methodology & Tools
-------------------

* **LiDAR + Camera:** These datasets include time-synchronized ``.pcd`` point clouds and ``.jpg`` images.
* **IMU + Camera:** Calibration was performed using `Kalibr <https://github.com/ethz-asl/kalibr/wiki/camera-imu-calibration>`_ with the `AprilTag target <https://github.com/ethz-asl/kalibr/wiki/downloads>`_.
* **Camera Intrinsics:** Calculated using a 70mm square checkerboard (6x8 target) via the `VINS-Fusion Camera Calibrator <https://github.com/HKUST-Aerial-Robotics/VINS-Fusion/tree/master/camera_models>`_.

Camera Intrinsic Calibration
----------------------------
The intrinsic parameters of the cameras, such as the camera model, camera matrix [K], and distortion parameters, 
were obtained using the camera calibration tool that is included in the VINS-Fusion package. 
The values obtained are presented below.

.. :math:`\begin{aligned}
.. & K = \begin{bmatrix}
.. a_{11} & a_{12} & a_{13} \\
.. a_{21} & a_{22} & a_{23} \\
.. a_{31} & a_{32} & a_{33}
.. \end{bmatrix} \\
.. &\text{This is some text below the matrix.}
.. \end{aligned}`

For Bell412 Datasets: 

.. literalinclude:: /images/cam_intrinsic_bell412.yaml
    :language: yaml

For DJI M600 Datasets:

.. literalinclude:: /images/cam_intrinsic_m600.yaml
    :language: yaml

IMU Intrinsic Calibration
-------------------------
The IMU parameters for both Bell412 and DJI M600 datasets are given below. 

.. literalinclude:: /images/imu_prams.yaml
    :language: yaml


Camera-IMU Extrinsic Calibration
--------------------------------
The camera-IMU transformation was found using Kalibr package.

For Bell412 Datasets: 

The down camera :math:`T_{BCd}` and front camera :math:`T_{BCf}`

.. literalinclude:: /images/T_BC_bell412.yaml
    :language: yaml

For DJI M600 Datasets:

The down camera :math:`T_{BCd}` and front camera :math:`T_{BCf}`

 .. literalinclude:: /images/T_BC_m600.yaml
    :language: yaml

Camera-LiDAR Extrinsic Calibration
----------------------------------
Down camera to LiDAR transfromation :math:`[T_{CLd}]` was found using Matlab LiDAR calibrator toolbox
and fine-tuned using manual realignment. 

For Bell412 datasets:

.. literalinclude:: /images/T_CL_bell412.yaml
    :language: yaml

For DJI M600 datasets: 

.. literalinclude:: /images/T_CL_m600.yaml
    :language: yaml

IMU-GNSS Extrinsic Calibration
------------------------------
IMU to GNSS transformation :math:`[T_{BG}]` for both Bell412 and DJI M600 datasets are given here. 

.. literalinclude:: /images/T_BG.yaml
    :language: yaml

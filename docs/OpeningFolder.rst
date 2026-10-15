Loading Tissue images
_____________________

Image Specifications and Fluorescent Staining
##############################################

A crucial step of the image processing done by AtlasXbrowser, is the location of the Region of Interest (ROI) of the image corresponding to the section of tissue where the A and B chips overlap. This is made much easier by flowing Bovine Serum Albumin (BSA) solution mixed with 
fluorescent dye through the outmost channels of both the A and B chips. These fluorescent colors will make it visually very
clear where the ROI is. As shown in the image below, the ROI is enclosed by this colored square.

*Note:* We recommend using two different colors of fluorescent dye on each chip to ensure the image is in correct orientation.

**NOTE** If using a purchased AtlasXomics kit, proper orientation would be to have the green channels on the left and top of the image.

The only image used for AltasXbrowser processing is the BSA image, with the fluorescent outside channels of the ROI in view.

**BSA Image:** Image taken using the epifluorescence setting of the microscope.


    .. figure:: /images/D223_BSA_image.png
       
        Above is the BSA image taken for AtlasXomics' internal run D223. Observe how the fluorescent lines of the outside channels are clearly visible in the image.

Image Folder Specifications
###########################

To use AtlasXbrowser for image processing, we recommend preparing a specific folder for hold all image contents pertaining to a particular run.

This image can be named anything. AtlasXbrowser currently supports .TIF, .png, and .jpg files.

    .. image:: /images/FolderCreated.png

See above how a new folder was created, storing the BSA (D223_postB_BSA.TIF) to be used by AtlasXbrowser.

Loading Image and Entering Metadata
###################################
In order to begin processing the tissue image, the first step is to load the relevant images.

#. Navigate to the *File* tab in the top left corner of the screen.

    .. figure:: /images/SelectingFile.png 

#. Select "Begin Image Processing".

    .. figure:: /images/BeginImageProcessing.png

#. Once selected a pop-up window should appear on screen.

    .. figure:: /images/OpeningImage_selectingMeta.png

**1.)** Select **File** in the first row of the pop-up titled, "Select BSA Image". Then navigate to the directory 
of the image folder, and select the BSA image.

**2.)** This button is used to select a custom barcode file. Automatically the default bc50v1-24 barcode file is selected. To Change this, select the currently labeled **bc50v1-24** and navigate to the desired custom barcode file.

    .. image:: /images/image_processing_revert.png

    Upon selecting a custom barcode file, if the user wants to revert to the default bc50v1-24 file, they can select the **Revert to bc50v1-24** circled above.

**3.)** Enter the desired name of the run (or data set) in the text box.

**4.)** In the **Tixel geometry** section of the **Selecting Images** window,
select the **Tixel size (µm)** that matches your chip. New sessions default to
10 µm. See :ref:`tixel-geometry` for the presets and custom dimensions.

**5.)** Once the image, barcode file, run ID and tixel geometry are configured,
select **Submit** to continue with image processing.

Upon selecting **Submit**, the popup should disappear and the BSA image should be loaded into the main window of the Browser.

This metadata will be saved and stored in the associated Spatial Folder for this experiment. Now we can proceed to configuring the image.

.. _tixel-geometry:

Tixel Size and Geometry
#######################

Set the geometry in the **Selecting Images** window before selecting **Submit**.
Choose a tixel size of **10**, **15**, **25** or **50 µm**. The presets are:

.. list-table:: Default tixel dimensions
   :header-rows: 1
   :widths: 20 25 25 30

   * - Tixel size (µm)
     - Capture width (µm)
     - Gap (µm)
     - Center-to-center pitch (µm)
   * - 10 (default)
     - 10
     - 15
     - 25
   * - 15
     - 15
     - 10
     - 25
   * - 25
     - 25
     - 25
     - 50
   * - 50
     - 50
     - 50
     - 100

The **capture width** is the width of a tixel's capture region. The **gap** is
the edge-to-edge distance between adjacent capture regions. Their sum is the
**center-to-center pitch**. For example, a 10 µm capture region with a 15 µm gap
has a 25 µm pitch.

Expand **Override tixel geometry** to enter a custom **Capture width (µm)** and
**Gap (µm)**. The capture width must be a finite, positive number; the gap must
be finite and zero or greater. The dialog previews the resulting pitch and
disables **Submit** while these values are invalid. These dimensions apply
uniformly across the chip.

Selecting another tixel size or clicking **Restore defaults** replaces the
custom dimensions with the selected preset. Collapsing the override section
only hides its fields; it does not reset the values. Use **Restore defaults**
to discard overrides.

Geometry controls determine the capture regions and their spacing within the
ROI. They do not change the channel count specified by the barcode file.
The selected dimensions are saved in the spatial folder; see
:ref:`saved-tixel-geometry` for details about reopening existing folders.

.. note::

   The image-loading screenshots show an earlier version of the dialog and do
   not include the tixel geometry controls.

Barcode File Selection
######################

As noted above, during the image loading process, the user is given the option to specify a custom barcode file to be used in AtlasXbrowser. The barcode file specified at this step is used when 
generating the *tissue_position_list.csv* file, as part of the spatial folder. To learn more about the contents of the spatial folder, please see the **Utilizing Spatial Folder** section of the documentation.

To view the barcode files that are included in the github repo, navigate to the "barcode_files".

.. figure:: /images/barcode_file_options.png

Shown above are the contents of the barcodes folder within the github repo of AtlasXbrowser.

* **yale_barcodes50** v1-v4: These are the barcodes used in the initial DBiT Paper published by The Fan Lab. The v1 - v4 indicate the orientation of these sequences.

  * v1: Standard Orientation
  * v2: Flipping the B chip barcodes relative to v1
  * v3: Flipping of the A chip barcodes relative to v1
  * v4: Flipping of both the A and B chip barcodes relative to v1

* **bc50v[1-2]-24**: These are the barcodes currently being used and recommended by AtlasXomics for ATAC seq. Two of the B chip barcodes have been replaced from the original Yale barcode batch.

  * The bv50v1-24.txt file is the default barcode file within AtlasXbrowser.
  * The v1 and v2 orientations of these barcode files match that listed above. Where v2 has flipped B chip barcodes relative to v1 and so forth.

Depending on the specific barcodes used in the DBiT process in the wetlab, any of these files can be selected during the image loading step.

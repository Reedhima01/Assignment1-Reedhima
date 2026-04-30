# Assignment1-Reedhima
Particle image Analysis using ImageJ for scientific Image Processing. 
Phase 1: Setup & Calibration

• Open Image: Drag and drop your file into ImageJ/Fiji.

• Set Scale: 

• Select the Straight Line tool.

• Draw a line exactly matching your scale bar on the image.

• Go to Analyze > Set Scale....

• Check Global if all your images were taken at the same magnification.

• Convert to 8-bit: 

• Go to Image > Type > 8-bit. (This is mandatory for thresholding).

Phase 2: Pre-Processing (Cleaning)

Goal: Remove "noise" so the software doesn't mistake dust for a particle.

• Subtract Background: 

• Go to Process > Subtract Background....

• Set the Rolling Ball Radius ( 50.0 pixels). This fixes uneven lighting.

• Smooth the Image: 

• Go to Process > Filters > Gaussian Blur....

• Set Sigma to 1.0 or 2.0. This blends "speckle" noise while keeping particle edges intact.

Phase 3: Segmentation (Binarization)

Goal: Tell the software exactly which pixels are "Object" and which are "Background."

• Threshold: 

• Go to Image > Adjust > Threshold....
• Upper limit : 255
• Lower limit : 90

• Click Apply. (Your image will now be strictly Black and White).

• Binary Cleanup: 

• Fill Holes: If your particles have white spots inside them, go to Process > Binary > Fill Holes.

• Watershed: If particles are touching, go to Process > Binary > Watershed. This draws a 1-pixel line to separate them.

Phase 4: Measuring & Counting

Goal: Extract the numerical data.

• Configure Measurements: 

• Go to Analyze > Set Measurements....

• Select: Area, Mean Gray Value, Shape Descriptors, and Display Label.

• Analyze Particles: 

• Go to Analyze > Analyze Particles....

• Size: Set a range to exclude noise ( 50-Infinity).

• Circularity: Leave at 0.4-1.00 unless you only want perfectly round objects.

• Show: Select Outlines.

• Check: "Display Results", "Clear Results", "Summarize", and "Add to Manager".

• Click OK.

Phase 5: Exporting & Saving

Goal: Secure your results for your lab report or publication.

• Save the Data Table: 

• In the Results window, go to File > Save As....

• Save as SampleName_Data.csv. (Use .csv so you can open it in Excel).

• Save the Visual Evidence: 

• A window titled "Drawing of [YourImage]" will appear with numbered particles.

• Go to File > Save As > Tiff.... (This proves which particles were counted).

• Save the ROI Set: 

• In the ROI Manager window, select all items (Ctrl+A).

• Click More >> Save....

• Save as SampleName_ROIs.zip.

# vitrual-try-on

A virtual try-on method takes a product image and an image of a model and produces an image of the model wearing the product. Most methods essentially compute warps from the product image to the model image and combine using image generation methods. However, obtaining a realistic image is challenging because the kinematics of garments is complex and because outline, texture, and shading cues in the image reveal errors to human viewers. The garment must have appropriate drapes; texture must be warped to be consistent with the shape of a draped garment; small details (buttons, collars, lapels, pockets, etc.) must be placed appropriately on the garment, and so on. Evaluation is particularly difficult and is usually qualitative.

# End to end virtual try on notebook


    Change runtime to GPU

    Resize the source images to h=256, w=192, and place them in my-source-input-images and in dataset/images folder of down-to-the-last-detail-with-detail-carving.

    Generate openpose json of these resized images and place them in dataset/pose_coco of down-to-the-last-detail-with-detail-carving.

    Select the cloth image, resize it to (h=256, w=192) and place it in cloth folder of down-to-the-last-detail-with-detail-carving.

    Generate the cloth mask of the resized cloth image using grabcut, and place it in cloth_mask folder of down-to-the-last-detail-with-detail-carving.

    Copy the resized images to images folder of my-source-input-images to images folder of $HOME/datasets/CIHP/

    Generate edges and labels using the code written and place them in CIHP/edges and CIHP/lables.

    To generate output of semantic parsing, update val.txt in list folder and val_id.txt.

    Run test_pgn.py and copy the output image in cihp_parsing_maps in format {image_name}_vis.png to parse_cihp of down-to-the-last-detail-with-detail-carving.

    Copy the label input images to parse_cihp of down-to-the-last-detail-with-detail-carving.

    Ensure all the input images are of size: h=256, w=192.

    Update the image names in demo.txt of down-to-the-last-detail-with-detail-carving.

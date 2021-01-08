# vitrual-try-on
End to end virtual try on notebook


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

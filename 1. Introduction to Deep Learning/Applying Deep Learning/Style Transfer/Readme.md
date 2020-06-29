Style transfer is basically allows me to take famous painting and recreate my own images in their style. The network learns the underlying 
techniques of those paintings and figures out how to apply them on its own.
For example: 

Photos: https://github.com/lengstrom/fast-style-transfer 
Video:  https://www.youtube.com/watch?v=xVJwwWQlQ1o

To try it out yourself, you can find the code in the fast-style-transfer GitHub repo. Either use git to clone the repository, or you 
can download the whole thing as a Zip archive and extract it.
The network has been trained on a few different styles [here](https://github.com/lengstrom/fast-style-transfer/tree/master/examples/style)
and saved into [checkpoint files](https://drive.google.com/drive/folders/0B9jhaT37ydSyRk9UX0wwX3BpMzQ). Checkpoint files contain all theinformation about the trained network to apply styles to new images.

Dependencies
-
For Windows, you'll need to install TensorFlow 0.12.1, Python 3.5, Pillow 3.4.2, scipy 0.18.1, and numpy 1.11.2

After installing Miniconda, open your command prompt. In there, enter these commands line by line:

conda create -n style-transfer python=3

activate style-transfer

conda install tensorflow scipy pillow

pip install moviepy

python -c "import imageio; imageio.plugins.ffmpeg.download()"

Transferring styles
-
- Download the Zip archive from the [fast-style-transfer repository](https://github.com/lengstrom/fast-style-transfer) and extract it. You can download it by clicking on the bright green button on the right.
- Download the Rain Princess checkpoint from [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/January/587d1865_rain-princess/rain-princess.ckpt_). Put it in the fast-style-transfer folder. A checkpoint file is a model that already has tuned parameters. By using this checkpoint file, we won't need to train the model and can get straight to applying it.
- Copy the image you want to style into the fast-style-transfer folder.
- Enter the Conda environment you created above, if you aren't still in it

Finally, in your terminal, navigate to the fast-style-transfer folder and enter
python evaluate.py --checkpoint ./rain-princess.ckpt --in-path <path_to_input_file> --out-path ./output_image.jpg (Note: Your checkpoint file might be named rain_princess.ckpt, notice the underscore, it's not the dash from above.)



The checkpoints were trained on the following paintings:
- Rain Princesss, by Leonid Afremov
- La Muse, by Pablo Picasso
- Udnie by Francis Picabia
- Scream, by Edvard Munch
- The Great Wave off Kanagawa, by Hokusai
- The Shipwreck of the Minotaur, by J.M.W. Turner

# Image Captioning with BLIP

Image Captioning is an `img2txt` model that leverages the BLIP architecture to generate descriptive captions for images. This tool automatically exports captions, making it easy to annotate visual content.

## Checkpoints

To run the model, ensure you have the necessary checkpoints. If the `checkpoints` folder does not exist, the script will automatically create it and download the model file. Alternatively, you can manually download the fine-tuned checkpoint and place it in the `checkpoints` folder.

**Download Link for BLIP-Large**: [BLIP-Large Checkpoint](<https://storage.googleapis.com/sfr-vision-language-research/BLIP/models/model_large_caption.pth>)

## Usage

You can generate captions using the command line interface (CLI) with the following syntax:

```bash
python inference.py [-h] [-i INPUT] [-b BATCH] [-p PATHS] [-g GPU_ID]
```

### Optional Arguments:
- `-h, --help`: Show help message and exit.
- `-i INPUT, --input INPUT`: Path to the input directory (e.g., `./images`).
- `-b BATCH, --batch BATCH`: Set the batch size for processing.
- `-p PATHS, --paths PATHS`: Specify a `.txt` file containing all image paths.
- `-g GPU_ID, --gpu-id GPU_ID`: Specify the GPU device to use (default is `0`). Can be `0, 1, 2` for multi-GPU setups.

### Example Command:
```bash
python inference.py -i /path/images/folder --batch 8 --gpu 0
```
## Preditive Results

Below is a collage of six images along with their generated captions:

| Image | Caption |
|-------|---------|
| ![019.jpg](images/image_019.png) |  |
| ![056.jpg](images/image_056.png) | A digital painting of a man with a futuristic face. |
| ![010.jpg](images/image_010.png) | A woman in a cat mask holding a sword. |
| ![1008.jpg](images/image_065.png) | A teacher standing in front of a classroom full of children. |
| ![1011.jpg](images/image_065.png) | A tortoise on a white background. |
| ![1014.jpg](images/image_065.png) | A glass of wine sitting on top of a table. |
| ![064.jpg](images/image_064.png) | A painting of a little girl with a bird on her head. |
| ![065.jpg](images/image_065.png) | A painting of a woman with glasses looking at the camera. |

<table>
  <tr>
    <td>
      <img src="images/image_019.png" alt="Cheese with Figs" width="300">
      <p>A woman in a costume holding two swords.</p>
    </td>
    <td>
      <img src="datasets/1002_small.jpg" alt="Yellow Flower" width="300">
      <p>A close-up of a yellow flower with a green background.</p>
    </td>
  </tr>
  <tr>
    <td>
      <img src="datasets/1005_small.jpg" alt="Colorful Flowers" width="300">
      <p>A planter filled with lots of colorful flowers.</p>
    </td>
    <td>
      <img src="datasets/1008_small.jpg" alt="Teacher and Students" width="300">
      <p>A teacher standing in front of a classroom full of children.</p>
    </td>
  </tr>
  <tr>
    <td>
      <img src="datasets/1011_small.jpg" alt="Tortoise" width="300">
      <p>A tortoise on a white background.</p>
    </td>
    <td>
      <img src="datasets/1014_small.jpg" alt="Glass of Wine" width="300">
      <p>A glass of wine sitting on top of a table.</p>
    </td>
  </tr>
</table>
## Contributing

Contributions are welcome! If you have major changes in mind, please open an issue first to discuss your ideas. 

Make sure to update the tests as appropriate to reflect your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

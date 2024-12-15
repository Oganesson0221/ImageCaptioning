# Image Captioning

This project generates captions for images using a pre-trained VisionEncoderDecoderModel from the `transformers` library. The model utilizes Vision Transformer (ViT) as the encoder and GPT-2 as the decoder to produce captions for input images.

## Prerequisites

Ensure you have Python 3.7 or higher installed along with `pip`. Additionally, a GPU is recommended for faster execution but not mandatory.

### Required Libraries

Install the required Python libraries by running:

```bash
pip install torch transformers pillow
```

### Verify Installation

To ensure all libraries are correctly installed, run:

```bash
python -c "import transformers, torch, PIL; print('All libraries are installed!')"
```

## Files

- **`caption.py`**: The main script for generating image captions.
- **`landing.jpg`**: Example image file to test the script.

## Instructions

1. Clone or download the repository:

   ```bash
   git clone https://github.com/your-repo/image-captioning.git
   cd image-captioning
   ```

2. Place the images you want to caption in the same directory as the script.

3. Run the script:

   ```bash
   python caption.py
   ```

4. The script will generate captions for the images and print them in the terminal.

### Example Output

If `landing.jpg` is used as input, the output might look like:

```
Final Caption is: ['a variety of fruits and vegetables laid out on a table']
```

## Customization

- **Input Images**: Modify the `predict_caption()` function call in `caption.py` to include your own image paths.

  Example:

  ```python
  predict_caption(['./my_image1.jpg', './my_image2.png'])
  ```

- **Hyperparameters**:
  Adjust the following variables in the script to experiment with model performance:
  - `max_length`: Maximum length of the generated caption (default: 16).
  - `num_beams`: Number of beams for beam search (default: 4).

## Troubleshooting

- **`ModuleNotFoundError`**: Ensure all required libraries are installed using the `pip install` command mentioned above.
- **CUDA Not Available**: If a GPU is not available, the script will default to using the CPU. This may result in slower performance.
- **Corrupted Images**: Ensure input images are valid and readable. Images in formats other than RGB will be automatically converted.

## References

- [Hugging Face Transformers Documentation](https://huggingface.co/docs/transformers)
- [VisionEncoderDecoderModel](https://huggingface.co/nlpconnect/vit-gpt2-image-captioning)

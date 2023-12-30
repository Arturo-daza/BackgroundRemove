# Background Remover

This Python script utilizes the `rembg` library to remove backgrounds from images in a specified input folder and organizes the processed images into an output folder.

## Usage

### Prerequisites

* Python 3.x
* Install dependencies with `pip install rembg`

### How to Use

1. Place the images you want to process in the `input` folder.
2. Run the script using the command `python backgroundremover.py`.
3. Processed images will be saved in the `output` folder, organized by the date and time of processing.

### Note

* Supported image formats: JPG, PNG, JPEG

## Script Details

The script is structured as a Python class `BackgroundRemover` with the following methods:

* `__init__(self, input_folder, output_folder)`: Initializes the class with input and output folders.
* `process_images(self)`: Processes images in the input folder, removes the background, and organizes the results in the output folder.
* `_remove_background(self, input_p, output_p)`: Uses the `rembg` library to remove the background from an image.
* `_move_originals(self, input_p, dest_p)`: Moves the original images to a subfolder named 'originals' within the processed folder.

## Example

```python
if __name__ == '__main__':
    input_folder = 'input'
    output_folder = 'output'

    background_remover = BackgroundRemover(input_folder, output_folder)
    background_remover.process_images()
```

Feel free to customize the script to fit your specific needs.

# Sudoku Solver
A sudoku solver that reads data from images.

This project implements a Sudoku solver using a combination of machine learning and image processing techniques. The solver takes an image of a Sudoku puzzle as input and provides the solved puzzle as output. The project consists of multiple Python scripts that work together to achieve this functionality.

## Features

- Solves Sudoku puzzles from images using image processing and machine learning.
- Utilizes a convolutional neural network (CNN) to classify digits in Sudoku puzzle cells.
- Implements image perspective transformation to extract the Sudoku grid from an input image.

## Prerequisites

Before running the code, ensure you have the following libraries and tools installed:

- Python 3.x
- PyTorch
- OpenCV
- NumPy

## Usage

1. Ensure you have a trained model for digit classification. You can train your own model using the provided `model.py` script or use a pre-trained model.
2. Run the `get_values.py` script and provide the path to an image containing a Sudoku puzzle. The script will extract the puzzle's values using image processing and the digit classification model.
3. Run the `solver.py` script to solve the Sudoku puzzle. The script uses a backtracking algorithm to find the solution.
4. The solved puzzle will be displayed, and you can verify the solution.

## Scripts

- `classifier.py`: Defines a classifier class that uses a pre-trained model to classify digits in Sudoku cells.
- `get_values.py`: Extracts Sudoku values from an input image using image processing and the digit classifier.
- `solver.py`: Solves a given Sudoku puzzle using a backtracking algorithm.
- `model.py`: Defines a CNN model for digit classification and exports the model to an ONNX file.

## Future Enhancements

This project can be expanded and improved in various ways:

- Developing a graphical user interface (GUI) for better user interaction.
- Integrating the image processing and solving steps into a single streamlined process.
- Enhancing the digit classifier model for better accuracy on various types of Sudoku puzzles.
- Optimizing the performance of the solver algorithm for larger puzzles.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to modify and adapt the code to suit your specific needs and explore further enhancements.



## To-do
- [ ] CV to load inputs
	- [ ] de-warp
		- [x] basic warp with contour detection
		- [ ] looking for grids with hough lines
	- [ ] digit classifier
		- [x] dataset
		- [x] model
		- [ ] training
	- [ ] merge modules
- [ ] solver
- [ ] merge modules
- [ ] solution overlay on live feed?

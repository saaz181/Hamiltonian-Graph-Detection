# Hamilton Graph Classification

## Project Overview
This project classifies images of graphs to determine if they are Hamiltonian graphs. A Hamiltonian graph contains a Hamiltonian cycle (a cycle that visits every vertex once and returns to the starting point). The goal is to create a model that can distinguish Hamiltonian graphs from non-Hamiltonian graphs using image data.

## Dataset
The [dataset](https://drive.google.com/drive/folders/1-1HAwCn3MhzQfLvoYV0aDaGOgSc2HUOn?usp=drive_link) consists of images of various graphs:
- Each image represents a graph structure.
- The train images are pre-labeled as Hamiltonian or non-Hamiltonian, serving as ground truth for model training and evaluation.

## Project Workflow

### 1. Data Loading and Preprocessing
- **Image Loading**: Loads graph images, possibly from folders organized by graph type.
- **Image Preprocessing**: Converts images to grayscale or binary format to simplify the graph structure.
- **Feature Enhancement**: Applies techniques like edge detection or noise reduction to highlight graph edges and nodes, making graph structures easier to analyze.

### 2. Feature Extraction
- **Graph Structure Detection**: Uses image processing to identify nodes and edges, potentially converting images to adjacency matrices or graph representations.
- **Cycle Detection**: Employs algorithms to detect cycles and evaluate connectivity. These features help identify Hamiltonian characteristics by revealing cycles that cover all nodes.

### 3. Model Design
- **Model Type**: Uses a Convolutional Neural Network (CNN) or other machine learning model to classify graphs.
- **Input Data**: The preprocessed images or extracted features are fed into the model.
- **Output**: The model outputs a binary classification indicating whether the graph is Hamiltonian.

### 4. Training the Model
- **Data Splitting**: Splits the data into training, validation, and testing sets.
- **Training Process**: Trains the model on labeled images, adjusting hyperparameters like learning rate, batch size, and epochs to optimize performance.
- **Loss and Optimization**: Uses a suitable loss function (e.g., binary cross-entropy) and optimizer to improve classification accuracy.

### 5. Evaluation
- **Metrics**: Evaluates the model using accuracy, precision, recall, and F1 score.
- **Validation**: Validates the model on the testing set to gauge performance on unseen images.
- **Error Analysis**: Examines misclassified graphs to identify areas for improvement.


## Code Structure

- `Hamilton.ipynb` contains the core logic for:
  - Loading and preprocessing the dataset
  - Defining and training the model
  - Running evaluations on the test data
  - (Optional) Functions for cycle detection and graph analysis

## Dependencies
- `numpy`: For numerical operations
- `pandas`: For creation of tables
- `PIL`: For image processing
- `pytorch`: For deep learning model implementation

## Future Improvements
- Enhance preprocessing to better detect edges and nodes.
- Experiment with other graph classification algorithms.
- Expand the dataset with more graph images for better model generalization.
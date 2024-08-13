# Auto Extraction of Manmade Topographic Features

This project aims to automate the extraction of manmade topographic features from satellite imagery using advanced AI and ML techniques. By leveraging deep learning models, specifically U-Net architectures, the project enhances the efficiency and accuracy of geospatial intelligence, with applications in military, defense, and urban planning.

## Project Overview

- **Objective**: Develop an AI-based solution to automatically identify and extract key manmade features such as building footprints, roads, and railway lines from satellite images.
- **Technologies Used**: Deep learning, U-Net architectures, AI/ML.
- **Applications**: Geospatial intelligence, military operations, infrastructure planning, emergency response.

## Methodology

1. **Data Collection and Preprocessing**: 
   - The dataset includes 72 aerial images of Dubai categorized into buildings, land, roads, vegetation, water, and unlabeled.
   - Images are cropped into smaller patches (256x256 pixels) and normalized to create a consistent dataset for training.

2. **Label Handling and Encoding**: 
   - RGB mask values are converted into integer labels for different classes.
   - One-hot encoding is applied to enable categorical segmentation during training.

3. **Model Architecture**: 
   - A modified U-Net model is used for semantic segmentation.
   - Includes dropout layers for regularization and the Jaccard coefficient for evaluating model performance.

4. **Custom Loss Function**: 
   - Combines Dice loss and categorical focal loss to handle class imbalance and improve robustness.

5. **Training and Evaluation**: 
   - The model is trained with the Adam optimizer, using metrics such as accuracy and the Jaccard coefficient to assess performance.
   - Visualizations of predictions compared to ground truth masks provide qualitative assessment.

## Results

The model achieved a Mean Intersection over Union (IoU) of approximately 0.670, indicating effective segmentation accuracy across multiple classes.

## Implications

This solution enhances military reconnaissance, surveillance, and strategic planning by providing timely and accurate geospatial information. The approach minimizes manual extraction efforts, reducing time and errors in decision-making processes.

## Future Directions

Future work involves expanding datasets and optimizing models for real-time applications. Integrating multi-sensor data will improve adaptability to various environmental conditions.

## Installation

1. Clone the repository:
   - `git clone https://github.com/yourusername/topographic-feature-extraction.git`
   - `cd topographic-feature-extraction`

2. Install dependencies:
   - Ensure you have the necessary Python packages installed. You can set up a virtual environment and install the dependencies using: `pip install -r requirements.txt`

3. Run the model:
   - Use the provided scripts and Jupyter notebooks to train and test the model on your dataset.

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Resources

- Dataset Link: https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery
- GitHub Repository: https://github.com/chiragtyagi2003/idex
- Colab Notebook: https://colab.research.google.com/drive/1rLcB5Q3Gc3BaTVIVpZ5bNmy0qEY4f_Ai?usp=sharing


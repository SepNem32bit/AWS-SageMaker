# Deploying a Hugging Face Model on AWS SageMaker

This script demonstrates how to deploy a pre-trained Hugging Face model for **question-answering** tasks on **AWS SageMaker**.

### Key Steps:
1. **Model Configuration**: Specifies the Hugging Face model (`distilbert-base-uncased-distilled-squad`) and task (`question-answering`).
2. **Model Deployment**: Creates a SageMaker endpoint using the `HuggingFaceModel` class with PyTorch and Transformers.
3. **Inference**: Sends input data (question and context) to the deployed endpoint and receives predictions.

### Prerequisites:
- An AWS account and a SageMaker execution role.
- Python installed with the `sagemaker` and `boto3` libraries.

### Example Usage:
- Input:
  ```json
  {
    "inputs": {
      "question": "What is used for inference?",
      "context": "This model is used with sagemaker for inference."
    }
  }

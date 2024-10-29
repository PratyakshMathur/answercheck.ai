# Automated Grading Tool: Project Plan

## Steps

### 1. Text Extraction with Computer Vision
- **Tools/Technologies**: Use Optical Character Recognition (OCR) tools such as:
  - Tesseract
  - Google Cloud Vision
  - AWS Textract

- **Preprocessing**: Implement image preprocessing techniques to improve OCR accuracy, especially for handwritten text. Consider:
  - Binarization
  - Noise reduction
  - Skew correction

- **Dataset**: A dataset of handwritten text is valuable for training or fine-tuning OCR models. Consider using public datasets like IAM or HWDB to improve accuracy on handwritten input.

### 2. NLP for Answer Similarity
- **Text Representation**: Represent answers and solution keys numerically using embeddings such as:
  - Word2Vec
  - GloVe
  - BERT or sentence-transformers for sentence-level representation

- **Similarity Measurement**: Use similarity measures to assess answer accuracy:
  - Cosine similarity
  - Jaccard similarity
  - Siamese networks for advanced similarity scoring

- **Thresholding**: Define grading thresholds based on similarity scores. Experiment with thresholds to enable partial and full credit.

### 3. Partial Grading
- **Scoring Mechanism**: Develop a mechanism to evaluate answer completeness. This could involve:
  - Checking for keywords/phrases
  - Using a model to assess content relevance

- **Feedback Generation**: Implement feedback functionality to help students understand areas of improvement based on their answers.

## Challenges

### 1. Extracting Messy Handwritten Text
- **Data Quality**: Collect diverse handwriting samples to improve model performance across different writing styles.
- **Error Handling**: Design a system to handle OCR errors, allowing:
  - Manual corrections
  - Flagging uncertain text for review

### 2. Implementing Partial Grading
- **Complexity**: Open-ended questions pose unique challenges. Consider breaking answers into components (e.g., main idea, supporting details) and scoring each part.
- **Model Training**: Training may require labeled data to specify how different answer types should be graded.
- **User Input**: Allow TAs to input grading criteria, enabling fine-tuning for different subjects or question types.

## Additional Considerations
- **User Interface**: Develop a user-friendly interface for TAs to upload exam papers, view results, and provide feedback.
- **Data Privacy**: Ensure compliance with data privacy regulations, especially when handling student data.
- **Testing and Validation**: Rigorously test with real exam papers to validate grading accuracy and feedback reliability.
- **Iterative Improvement**: Consider a feedback loop where TAs can provide feedback on grading results, allowing continuous model improvement.

By following these structured steps and addressing the outlined challenges, you’ll be well-equipped to create a robust web application that enhances grading efficiency for TAs.

Good luck with your project!
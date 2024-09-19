# Translation
# English to Arabic Translator

## Overview
This project implements an English to Arabic translation model using a sequence-to-sequence architecture with Keras. The model is trained on a custom dataset, allowing for translation of English sentences into Arabic.

## Requirements
To run this code, you will need the following libraries:
- Keras
- NumPy
- Gradio (optional)

You can install the required libraries using:
```bash
pip install numpy keras gradio
```

## File Structure
- `ara.txt`: The training dataset containing English-Arabic sentence pairs.
- The script provided in this repository which includes the model training and inference code.

## Usage

1. **Load Data**: The model reads from `ara.txt`, which should contain tab-separated English and Arabic sentence pairs.

2. **Preprocessing**: The data is tokenized and vectorized to prepare for model training.

3. **Model Training**: The model is trained using LSTM layers with specified batch size and epochs.

4. **Model Inference**: After training, the model can be used to translate sentences.

5. **Translation Function**: The `translate` function processes input text and generates translations using the trained model.

## Gradio Interface
**Note**: The Gradio section of the code is not working well and may require adjustments to function correctly. Specifically, the translation function may not handle input preprocessing as intended.

To use the Gradio interface:
- Ensure the Keras model is loaded.
- Start the interface using `iface.launch()`.

## Example of Running the Model
You can test the translation with the following loop:
```python
for seq_index in range(20):
    input_seq = encoder_input_data[seq_index: seq_index + 1]
    decoded_sentence = decode_sequence(input_seq)
    print("-")
    print("Input sentence:", input_texts[seq_index])
    print("Decoded sentence:", decoded_sentence)
```

## Important Notes
- Make sure the `ara.txt` file is available at the specified path.
- Adjust the Gradio `translate` function to ensure input sequences are properly formatted before passing to the model.


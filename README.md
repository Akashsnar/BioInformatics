# Mutation Prediction for Coronaviruses Using Genome Sequence and Recurrent Neural Networks

## Project Overview
This project aims to predict potential future mutations in the genome sequences of coronaviruses, such as SARS-CoV-2, using deep learning models. Accurate prediction of these mutations is crucial for preparing effective public health measures, updating vaccines, and anticipating new variants that could impact the global population.

## Motivation
Coronaviruses are highly mutable, evolving rapidly and acquiring new mutations that can affect transmissibility, virulence, and resistance to current treatments or vaccines. Predicting future mutations supports early intervention, aiding in the development of proactive therapeutic and preventive strategies.

## Approach
The project leverages Long Short-Term Memory (LSTM) Recurrent Neural Networks (RNNs) to analyze time-sequenced genome data. This architecture is chosen due to its capability to capture long-term dependencies and patterns within sequential data, making it ideal for genomic sequence analysis.

### Data Collection and Preparation
- **Data Source**: Genome sequences were collected from the National Center for Biotechnology Information (NCBI) database in FASTA format.
- **Preprocessing Steps**:
  1. Removal of header parts.
  2. Elimination of newline characters.
  3. Padding sequences as needed with 'A'.
  4. Encoding the genome sequences using one-hot encoding: `{'A': [1, 0, 0, 0], 'T': [0, 1, 0, 0], 'C': [0, 0, 1, 0], 'G': [0, 0, 0, 1]}`.

### Model Architecture
- The LSTM-RNN model is built to address challenges like the vanishing gradient problem found in traditional RNNs.
- **Key Components**:
  - Input gate, forget gate, and output gate regulate the flow of information.
  - Trained using backpropagation through time (BPTT) with the Adam optimizer.

### Results
- The LSTM-RNN model, when trained on large datasets of coronavirus genome sequences, demonstrated accuracy in predicting mutation locations and types.
- **Merits**:
  - Provides early warning for potential mutations, aiding vaccine and treatment updates.
- **Limitations**:
  - Model performance depends on the availability of high-quality data.
  - Training is computationally intensive.

## Conclusion
The LSTM-RNN model shows promise in predicting future mutations, enhancing preparedness for emerging variants. Ongoing work aims to improve model accuracy and efficiency, contributing to better forecasting and public health planning.

## Authors
- Pranesh S
- Bishwadip Maitra
- Anmol Kumar Pandey
- Akash Narvariya
- Mohd. Rizwan

## References
1. **Base Paper**: Mutation Prediction for Coronaviruses Using Genome Sequence and Recurrent Neural Networks by Pranav Pushkar et al.
2. **Supporting Literature**: Various studies and models such as PRIEST and MutaGAN for viral mutation prediction.

## Future Work
- Enhance the accuracy of the model through additional data and architectural improvements.
- Explore additional techniques for mutation prediction and generalize the approach for other viruses.



For detailed information, data, and results, please refer to the full project documentation.

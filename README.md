# Medical Drug Classification System

A machine learning system that classifies drugs based on their primary medical conditions using a fine-tuned GPT model.

- Google Slides: https://docs.google.com/presentation/d/1i1IAywC3Lu3CwfGmO9eUQStwEIZ1RBC5pmP-Ld4ikXU/edit?usp=sharing
- Google Slides (PDF): https://drive.google.com/file/d/1d8xD0Dd70ui3kLHVJojhekTeNaVzSqZ8/view?usp=sharing

## Overview

This system takes drug names as input and predicts which medical conditions they're primarily used to treat. It uses OpenAI's GPT-3.5-turbo model fine-tuned on a custom medical dataset.

## Features

- Drug classification into 8 medical categories:
  - Acne
  - ADHD
  - Allergies
  - Alzheimer's
  - Amoebiasis
  - Anaemia
  - Angina

- Support for various drug formats:
  - Tablets
  - Capsules
  - Syrups
  - Injections
  - Topical medications
  - Other formulations

## Technical Requirements

python:requirements.txt
pandas>=2.0.0
openpyxl>=3.1.0
openai>=1.0.0
python-dotenv>


## Dataset

The training dataset consists of drug names paired with their primary medical conditions. The data is formatted as JSONL for fine-tuning the GPT model. Each entry contains:
- Drug name with formulation details
- Medical condition classification (0-6)
- System prompt and conversation format

## Model Architecture

- Base Model: GPT-3.5-turbo
- Fine-tuning: Custom medical dataset
- Input Format: Conversational (system & user messages)
- Output: Numerical classification (0-6)

## Usage

1. Install dependencies:

```
bash
pip install -r requirements.txt
```


2. Set up environment variables:

```
bash
OPENAI_API_KEY=your_api_key_here
```

3. Prepare your drug data in the required format
4. Run the classification system
5. Get predictions for medical conditions

## Data Format

Input format example:

```
json
{
"messages": [
{"role": "system", "content": "You are a helpful medical assistant."},
{"role": "user", "content": "Drug: [Drug Name]\nMalady:"},
{"role": "assistant", "content": "[Classification]"}
]
}
```

## Classification Mapping

```
json
{
"Acne": 0,
"Adhd": 1,
"Allergies": 2,
"Alzheimer": 3,
"Amoebiasis": 4,
"Anaemia": 5,
"Angina": 6
}
```

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- OpenAI for the GPT-3.5-turbo model
- Contributors to the medical dataset
- Open source community for tools and libraries

## Contact

For questions and support, please open an issue in the GitHub repository.

# Autoencoders

This section of the project contains the various autoencoder-based attempts to create hybrid objects.

# Contents

## CIFAR10 + CARS dataset:
The CIFAR10 + CARS dataset contains background-filtered images of cars, cats, dogs, and horses.

- `cars-setup.sh`: a shell script that sets up data for the CIFAR10 + CARS files.
- `CARS.py`: Python file that contains everything needed to run the CIFAR10 + CARS model
- `cars.ipynb`: Jupyter notebook that contains logic for running the CIFAR10 + CARS model
- How to run:
  - Run `bash cars-setup.sh` to download and extract data
  - Run `python3 CARS.py` to train the model and display the results
  - Alternatively, open `cars.ipynb` with Jupyter, which offers similar functionality as the latter

## CIFAR10 dataset:
For the CIFAR-10 dataset, we made several different models.

- CIFAR V1 is a basic convolutional neural network, with the encoder and decoder trained simultaneously.
  - `CIFAR_v1.py`: Python file that contains all required logic to run this model
  - How to run:
    - Run `python3 CIFAR_v1.py` to download data, train the model, and display the results.
- CIFAR V2 is the best-working model. For this model, we train the encoder (as a classifier, trying to separate the classes in encoded space) and decoder separately.
  - `cifar-get-pretrained-models.sh`: a shell script that will download all of our pretrained models for CIFAR V2
  - `CIFAR_v2.py`: Python file that contains everything needed to run the CIFAR V2 model
  - `CIFAR-separate-training.ipynb`: Jupyter notebook that contains logic for running the CIFAR V2 model
  - How to run:
    - Run `bash cifar-get-pretrained-models.sh` to download the pretrained models
    - Run `python3 CIFAR_v2.py` to download data, train the model, and display the results.
    - Alternatively, run `python3 CIFAR_v2.py <model_name_here>` to display the results of the model given the pretrained model `<model_name_here>`
      - For example, `python3 CIFAR_v2.py cifar-v2-model-4.pth`
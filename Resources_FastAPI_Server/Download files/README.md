### Vehicle Damage Detection Backend Server

This code is for FastAPI server that takes car image as an input and predicts if it has a damage or not.
It has a single end point called `predict` which takes input file and returns a response in this format,
```commandline
{
    "prediction": "Rear Breakage"
}
```

### Model Details
1. Used ResNet50 for transfer learning
2. Model was trained on around 1700 images with 6 target classes
   1. Front Normal
   1. Front Crushed
   1. Front Breakage
   1. Rear Normal
   1. Rear Crushed
   1. Rear Breakage
9. The accuracy on the validation set was around 80%

### Set Up

1. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
   
2. Run the fast api server:
   ```commandline
   fastapi dev server.py

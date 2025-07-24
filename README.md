# Plants_Classification
This project includes the Files, Model and Dataset for an AI that can classify up to 30 different types of fruit.

The dataset contains approximately 3100 images and the model was run through 34 epochs to reach around 70-80% accuracy on average.
The AI works by comparing the given images to the other images in it's dataset, then determining its similarity or probabilty to be a certain class of object.
The Files for the dataset can be found in "PlantsDataSet" and the model can be found in "PlantsModel"
The AI model can be modified by adding new pictures the accuracy of the model can be improved by running the AI through more epochs

To run this project, open the terminal.
Locate the Image you want to run through the program and run the command:
"imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/[Where the file is found] [What the file will be called after running through the AI model]"
Once the command is finised running, the result will appear in the sidebar in VScode.

To train the model further, 
Open the doc using "./docker/run.sh"
Change directories "cd python/training/classification"
And run the command to retrain the model "python3 train.py --model-dir=models/PlantsModel data/PlantsDataSet"
This will result in the model running through around 34 epochs. You can press Cntrl + C to end the program early, as it will take a few hours

The dataset used for this model was from "Marquis03" on Kaggle: https://www.kaggle.com/datasets/marquis03/plants-classification

Example of the AI's classification: https://github.com/user-attachments/assets/ab5a4ff7-1978-45b7-ab7a-a0df285691fa

Link to a video explanation: https://github.com/user-attachments/assets/509dce88-3299-4030-9380-64ab40732f13

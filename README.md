# Recreating Retina U-Net
This repository holds our attempts at recreating the experiments conducted in [Retina U-Net: Embarrassingly Simple Exploitation of Segmentation Supervision for Medical Object Detection](https://proceedings.mlr.press/v116/jaeger20a/jaeger20a.pdf)

Summary of our Attempts:
- Failed: Attempt 1: We began by using the publicly available LIDC-IDRI dataset in an effort to replicate the experiments directly.
- Failed: Attempt 2: We recreated the synthetic ToyDataset as described in the paper and attempted to integrate it with the PyHealth library.
- Successful: Attempt 3: We recreated the ToyDataset and experiments as closely as possible to the original Retina U-Net paper, but without forcing integration with PyHealth.

**Attempt 3 was the most successful, therefore it is the code we used to gather our results and make our conclusions**

## How To Run Our Code
Each Attempt we made is stored in it's own Attempt .pynb file to make running as simple as possible:

1. Click on an Attempt .pynb file and click the "Open in Colab" button in the preview to see our code in a Google Colab Workspace.
<img width="1110" alt="Screen Shot 2025-05-05 at 10 29 19 AM" src="https://github.com/user-attachments/assets/c53094b7-57c9-404e-a01a-4b3b9a6e4e84" />
2. Change the Runtime to the T4 GPU (Runtime -> Change runtime type -> T4 GPU -> Save):

![Screen Shot 2025-05-05 at 10 34 40 AM](https://github.com/user-attachments/assets/8946f124-a6df-4a95-8bb6-00a053498eac) 

![Screen Shot 2025-05-05 at 10 39 37 AM](https://github.com/user-attachments/assets/f1b87d61-3c05-449a-ab15-838d8ba9f899)

And Make sure that you see that you are connected to the T4 GPU in the right-hand corner:

![Screen Shot 2025-05-05 at 10 42 19 AM](https://github.com/user-attachments/assets/89e4b8da-0700-479b-9344-e694700ebf4f)

3. Finally, run all the code! (Runtime -> Restart session and run all):
![Screen Shot 2025-05-05 at 10 45 52 AM](https://github.com/user-attachments/assets/0871f437-7339-464f-9c3e-214ce3e06e24)

Disregard the warning messages (Are you sure you want to restart runtime and Not authored by Google Workspace) and proceed.

## Results

Quantitative:


| Model              |  Mean Dice Score | 
| ------------------ | ---------------- | 
| Retina U-Net       |   **0.9878**     | 
| Retina Net         |     0.9043       |
| U-Net              |     0.8871       |



Qualitative:

Baseline U-Net Model Results:

![UNetCircleResult](https://github.com/user-attachments/assets/4823d6f8-7527-4eb2-a6db-72e0a78c6974)

![UNetRingResult](https://github.com/user-attachments/assets/4a7c3ca9-6c97-4a66-a528-18643529cbbc)

Baseline Retina Net Model Results:

![RetinaNetCircleResult](https://github.com/user-attachments/assets/d2345fa5-3dbb-47af-a236-ca6773eee0e2)

![RetinaNetRingResult](https://github.com/user-attachments/assets/79cd518e-1b21-4671-a9e1-72cd45e6d725)

Retina U-Net Model Results:

![RetinaUNetCircleResult](https://github.com/user-attachments/assets/e9a650aa-5a31-4ff1-836f-042429423b01)

![RetinaUNetRingResult](https://github.com/user-attachments/assets/6f926b83-720c-4b06-bd9c-8b59803ac6ba)



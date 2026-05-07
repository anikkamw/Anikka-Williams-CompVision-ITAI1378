# AI Usage Log

## 1. Architectural Pivot (ViT to YOLOv8)
- **Date**: April 20, 2026
- **Tool Used**: Gemini
- **Question Asked**: "Is Vision Transformer (ViT) or YOLOv8 better for a project requiring < 2.0s real-time detection?"
- **What I Learned**: I learned that while ViT is powerful for classification, YOLOv8 (You Only Look Once) is specifically architected for real-time object detection. It processes images in a single pass, making it significantly faster for clinical triage.
- **How I Applied It**: I pivoted my entire project from a simple classifier to a YOLOv8 Nano detection system to ensure I met my speed goals.

## 2. Debugging Data Loading and Pathing
- **Date**: May 1, 2026
- **Tool Used**: Gemini
- **Question Asked**: "How do I move specific folders from two different Kaggle datasets into one master project folder in Colab?"
- **What I Learned**: I learned how to use the `shutil` and `os` libraries to create directories and copy files. I also learned how to handle hidden paths when using `kagglehub`.
- **How I Applied It**: I used this to combine the Dog Skin Disease dataset with the Human Scabies dataset into a single 'mange_project' folder with three distinct classes.

## 3. Custom Python Validation Split
- **Date**: May 2, 2026
- **Tool Used**: Gemini
- **Question Asked**: "How can I move 10% of my images and labels into a validation folder if my dataset exported as 100% training?"
- **What I Learned**: I learned how to use the `random` library to select a subset of files and the `os.path.join` method to ensure images and their corresponding `.txt` labels moved together.
- **How I Applied It**: I wrote and ran a custom Python script in my notebook to create a `/valid` folder, which allowed the YOLO engine to perform proper validation during the training process.

## 4. Data Quality Audit & Duplicate Removal
- **Date**: May 3, 2026
- **Tool Used**: Gemini
- **Question Asked**: "Why is my Scabies accuracy lower than expected even after 25 epochs?"
- **What I Learned**: I learned about "data leakage" and how duplicate images can skew results and hide model weaknesses. I learned that scientific validity requires a diverse, unique image set.
- **How I Applied It**: I performed a manual audit in Roboflow based on this advice, removing duplicates to ensure 209 unique images for Version 2, which led to more reliable model performance.

## 5. Failure Analysis and Logic Errors
- **Date**: May 5, 2026
- **Tool Used**: Gemini
- **Question Asked**: "Why is my model failing to detect Scabies even though the training loss is low?"
- **What I Learned**: I learned about the concept of "low contrast" failures and how background noise can confuse a model. We identified that the Scabies images often blended into the skin color, unlike the more distinct Demodectic lesions.
- **How I Applied It**: I documented this in my final presentation as a Logic Error.

## 6. Performance Benchmarking & Visualization
- **Date**: May 6, 2026
- **Tool Used**: Gemini
- **Question Asked**: "How do I interpret the YOLO inference speed logs and visualize hidden results?"
- **What I Learned**: I learned how to read the three-part speed log (preprocess, inference, postprocess). I also learned how to use `matplotlib` to "force-visualize" bounding boxes stored in hidden directories.
- **How I Applied It**: I used these metrics to prove my system achieved a **3.2ms inference speed**, far exceeding the 2.0s requirement. I also generated the final visualization images used in my README.

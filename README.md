# Brain-MRI-Tumor-Dectection
Brain Tumor Classification and Detection
Using Machine Learning

Table of Contents
Overview
This project implements advanced machine learning techniques for the detection and classification of brain tumors using medical imaging data. It uses object classification and object detection models to for brain MRI scans analysis.

Features
Data Processing: Utilizes the Mahadih534 brain tumor dataset for training and evaluation.
Model Implementation: Includes both classification and detection models for comprehensive tumor analysis.
Visualization: Generates output images for model analysis, tumor, and non-tumor cases.
Evaluation: Provides tools for assessing model performance and accuracy.
Workflow
The project follows a structured workflow for analyzing brain MRI scans and detecting tumors. The main workflow is controlled by the analysis_workflow() function, which orchestrates the following steps:

Dataset Loading:

The workflow can either load the dataset from a source (e.g., "Mahadih534/brain-tumor-dataset") or from a previously saved local copy.
Controlled by workflow_config['load_dataset'] and workflow_config['load_dataset_from_disc'].
Data Exploration and Visualization:

Display sample images from the dataset.
Explore dataset statistics and features.
Generate and save visualizations of tumor and non-tumor samples.
Controlled by various flags in workflow_config, such as display_images, explore_dataset, get_all_labels, etc.
Model Application:

Apply classification and/or detection models to the dataset.
The workflow supports both types of models, controlled by the choose_model dictionary.
Classification model: "Devarshi/Brain_Tumor_Classification"
Detection model: "DunnBC22/yolos-tiny-Brain_Tumor_Detection"
Result Analysis and Visualization:

Generate output images showing model predictions.
Save results in the output_images directory, organized by model type (classification/detection).
Performance Comparison (optional):

Compare execution times of models on CPU vs GPU.
Controlled by workflow_config['compare_models'].
Workflow Configuration
The workflow is highly configurable through the workflow_config dictionary:

workflow_config = {
    'load_dataset': False,
    'load_dataset_from_disc': True,
    'display_images': False,
    'display_and_save_images': False,
    'explore_dataset': False,
    'get_all_labels': False,
    'inspect_features': False,
    'get_tumor_samples': False,
    'apply_model': True,
    'compare_models': False
}

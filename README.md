
# Data Visualization with Amazon QuickSight and S3

## Project Overview: _[Project Link ](https://github.com/sid-7878/AWS-Quick-Sight-And-S3-Services/blob/main/AWS%20Project.pdf)_  
This project demonstrates how to create a dashboard using **Amazon QuickSight** and data stored in an **AWS S3 bucket**. The dashboard provides centralized tools for monitoring, analyzing, and visualizing key metrics and data points, enabling organizations to make informed decisions based on real-time data.

## Features
- Utilizes **Amazon S3** for data storage.
- Leverages **Amazon QuickSight** for creating interactive dashboards.
- Processes the `amazon-bestseller-dataset` to generate meaningful visualizations.

## Steps to Build the Dashboard

### 1. **Setup S3 Bucket**
- Navigate to the **S3 service** in the AWS Management Console.
- Create a bucket with a unique name (e.g., `siddhi-amazon-project`).
- Upload the following to the S3 bucket:
  - `amazon-bestseller-dataset`
  - A manifest JSON file linking the data stored in the bucket.

### 2. **Prepare the Manifest File**
- Create a manifest file with the bucket name and dataset details.
- Example Manifest File:
  ```json
  {
    "fileLocations": [
      {
        "URIPrefixes": [
          "s3://siddhi-amazon-project/amazon-bestseller-dataset/"
        ]
      }
    ],
    "globalUploadSettings": {
      "format": "CSV",
      "delimiter": ",",
      "textQualifier": "\"",
      "containsHeader": "true"
    }
  }
  ```
- Edit the file using tools like **VS Code** and upload it to the S3 bucket.

### 3. **Setup Amazon QuickSight**
- Search for **Amazon QuickSight** in the AWS Management Console and sign up.
- In the QuickSight dashboard:
  - Select **Datasets** > **New Dataset**.
  - Choose **S3** as the data source.
  - Copy the manifest file URL from the S3 bucket and paste it into QuickSight.
  - Name the data source and click **Connect**.

### 4. **Visualize the Data**
- Click on **Visualize** to start creating dashboards.
- Drag and drop fields (e.g., `Brand`) to create visualizations.

### 5. **Sample Output**
- Example dashboard showcasing insights from the dataset.

## Tools Used
- **Amazon S3**: For secure data storage.
- **Amazon QuickSight**: For creating interactive dashboards.
- **VS Code**: For editing the manifest file.

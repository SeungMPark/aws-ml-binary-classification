# aws-ml-binary-classification
Lab to illustrate using Amazon Machine Learning to diagnose breast cancer in patients (binary classification)

![Lab Environment](https://user-images.githubusercontent.com/3911650/33621769-23e78db4-d9a9-11e7-87ae-a6ba7ee1bd71.png)

## Getting Started
Deploy the CloudFormation stack in the template in `infrastructure/`. The template creates a user with the following credentials and minimal required permisisons to complete the Lab:
- Username: _student_
- Password: _password_

## Instructions
- Get the URL of the CSV data file automatically uploaded to S3
- In the Amazon ML Console, launch the standard setup wizard to:
    - Create a datasource from the CSV file in S3
        - Change the diagnosis column to be of type Binary, and use the id column as a row ID
    - Create a model with default values
    - Create an evaluation with default values
- Inspect the datasource and evaluation statistics
- Perform a real-time prediction by pasting in the following record: `000,13.24,14.06,87.16,563.3,0.09679,0.08229,0.06864,0.04791,0.1685,0.05966,0.2599,0.7686,2.158,22.56,0.008962,0.0136,0.02287,0.01415,0.0188,0.0023,15.11,19.26,99.7,711.2,0.144,0.1773,0.239,0.1288,0.2977,0.07259`

## Cleaning Up
In the Amazon ML Console, delete the datasource, model, and evaluation. Delete the CloudFormation stack to remove all the remaining template resources.

## Acknowledgments
Thank you to the creators of the [Wisconsin Diagnostic Breast Cancer dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29) and the [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php) for hosting the original data for all.
# API Testing with Postman & Newman

This repository contains a collection of API tests using Postman and automated via Newman. The purpose of this project is to automate API testing and generate comprehensive reports that can be integrated into CI/CD pipelines.

## Prerequisites
Before running the tests, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v12 or higher)
- [Newman](https://www.npmjs.com/package/newman)

To install Newman globally, use the following command:
npm install -g newman

## Setup Instructions
1)Clone the repository:
git clone https://github.com/Mdeliaskhan04/Practice-API-Testing.git
cd repo-name

2)Install the Newman HTML reporter:
npm install -g newman-reporter-htmlextra

3)Export Postman collection:
In Postman, open the collection you want to run.
Click the ellipsis (...) next to the collection name and select Export.
Choose the Collection v2.1 format and save it to the collections/ directory in this repository.

4)Export Postman environment (if required):
Similarly, export any environment variables your collection may need and save the file to the environments/ directory.

## How to Run Tests
1)To execute the Postman collection using Newman, run the following command in your terminal:
newman run collections/<collection-file>.json

2)If your tests depend on an environment, add the environment file using:
newman run collections/<collection-file>.json -e environments/<environment-file>.json

## Generating HTML Reports
1)To generate detailed HTML reports after running the tests, use the following command:
newman run collections/<collection-file>.json -r htmlextra --reporter-htmlextra-export reports/report.html

## Environment Variables
If your collection uses environment variables, make sure to export your environment from Postman. You can then run the tests with the specified environment like this:

newman run collections/<collection-file>.json -e environments/<environment-file>.json -r htmlextra --reporter-htmlextra-export reports/report.html

## License
This project is licensed under the MIT License. See the LICENSE file for details.

### Explanation:
- **Prerequisites**: Lists Node.js and Newman as essential tools.
- **Setup Instructions**: Guides on how to set up Newman, export collections from Postman, and install the required dependencies.
- **How to Run Tests**: Provides the command to run the tests, with or without environment variables.
- **Generating HTML Reports**: Explains how to generate a detailed HTML report.
- **Environment Variables**: Includes instructions for handling Postman environments.
- **License**: A placeholder for the license of the project.

You can replace placeholders like `<collection-file>.json` with your specific

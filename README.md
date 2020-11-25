# ServerlessWebPageLambda

Requirements :
- AWS account


Architecture :

<img src="https://miro.medium.com/max/1200/1*L28ihnevjQK9O2U_vBgaHA.png" width="700" height="400" style="margin-left: auto; margin-right: auto;" />


1) Create Lambda function
- "Runtime" : choose Python 3.6
- Put Python code

2) Create API Gateway
- API type : HTTP API
- Security : Open
- "Additionnal settings"
- Change name
- Enable Cross-origin resource sharing (CORS)
- Click "Add"

3) Configure API Gateway
- Go to "Develop" > "Routes"
- "Create" new route
- Method : /GET
- Path : /YOUR_LAMBDA_FUNCTION_NAME
- Click "ANY" > "Delete"
- Click "GET" > Integration > "Configure" your lambda function
- Go to "Deploy" > "Stages"
- Select "default" and click "Deploy"

4) Configure S3 Bucket to host web page
- Go to S3 and create S3 Bucket
- Add HTML files, make them "public"

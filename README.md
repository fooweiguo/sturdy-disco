# sturdy-disco
Change #1. 

```
git add .
git commit -m "message here"
git push
```

To initialize the node application and run testing offline
```
npm init
npm install -g serverless
npm install serverless-offline --save-dev (to install serverless-offline plugin).
serverless.cmd offline start
```

Then on the browser type localhost:3000 to see the message. 

Once this is done, we are ready to deploy it to AWS account. We need to run:

```
serverless deploy
```

Then go to AWS console > Cloud Formation and then find the sturdy-disco serverless. Afterwards go to AWS Lambda to find the sturdy-disco application > API Gateway > Configurations > API endpoints to find the endpoint leading to the message. After it is done, we are ready to destroy all the resources:

```
serverless remove
```


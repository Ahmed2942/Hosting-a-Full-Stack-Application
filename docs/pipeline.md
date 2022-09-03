# Pipeline Process
## Jobs
### Build Job
- Build Job starts by running docker image and preparing it with installing nodejs, providing checkout github functionality. 
- It runs some scripts that build our application environment and install its node modules and make it ready for deployment.
- Install node
```
- node/install:
    node-version: '14.15'      
```
- Checkout our github repo
```
- checkout
```
- Install Front-End Dependencies.
```
npm run frontend:install
```
- Install API Dependencies
```
npm run api:install
```
- Front-End Lint
```
npm run frontend:lint
```
- Front-End Build
```
npm run frontend:build
```
- API Build
```
npm run api:build
```
### Deploy Job
Deploy Job starts by running docker image and preparing it with installing aws cli, aws elastic beanstalk and nodejs, providing checkout github functionality.
- Install node
```
- node/install:
    node-version: '14.15'      
```
- Install aws-cli
```
- aws-cli/setup      
```
- Install eb-cli
```
- eb/setup  
```
- Install node
```
- node/install:
    node-version: '14.15'      
```
- Checkout our github repo
```
- checkout
```
- Deploy App
```
npm run deploy
```


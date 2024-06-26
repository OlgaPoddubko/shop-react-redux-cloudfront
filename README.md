# React-shop-cloudfront

This is frontend starter project for nodejs-aws mentoring program. It uses the following technologies:

- [Vite](https://vitejs.dev/) as a project bundler
- [React](https://beta.reactjs.org/) as a frontend framework
- [React-router-dom](https://reactrouterdotcom.fly.dev/) as a routing library
- [MUI](https://mui.com/) as a UI framework
- [React-query](https://react-query-v3.tanstack.com/) as a data fetching library
- [Formik](https://formik.org/) as a form library
- [Yup](https://github.com/jquense/yup) as a validation schema
- [Serverless](https://serverless.com/) as a serverless framework
- [Vitest](https://vitest.dev/) as a test runner
- [MSW](https://mswjs.io/) as an API mocking library
- [Eslint](https://eslint.org/) as a code linting tool
- [Prettier](https://prettier.io/) as a code formatting tool
- [TypeScript](https://www.typescriptlang.org/) as a type checking tool

## Available Scripts

### `start`

Starts the project in dev mode with mocked API on local environment.

### `build`

Builds the project for production in `dist` folder.

### `preview`

Starts the project in production mode on local environment.

### `test`, `test:ui`, `test:coverage`

Runs tests in console, in browser or with coverage.

### `lint`, `prettier`

Runs linting and formatting for all files in `src` folder.

### `client:deploy`, `client:deploy:nc`

Deploy the project build from `dist` folder to configured in `serverless.yml` AWS S3 bucket with or without confirmation.

### `client:build:deploy`, `client:build:deploy:nc`

Combination of `build` and `client:deploy` commands with or without confirmation.

### `cloudfront:setup`

Deploy configured in `serverless.yml` stack via CloudFormation.

### `cloudfront:domainInfo`

Display cloudfront domain information in console.

### `cloudfront:invalidateCache`

Invalidate cloudfront cache.

### `cloudfront:build:deploy`, `cloudfront:build:deploy:nc`

Combination of `client:build:deploy` and `cloudfront:invalidateCache` commands with or without confirmation.

### `cloudfront:update:build:deploy`, `cloudfront:update:build:deploy:nc`

Combination of `cloudfront:setup` and `cloudfront:build:deploy` commands with or without confirmation.

### `serverless:remove`

Remove an entire stack configured in `serverless.yml` via CloudFormation.

Task 2.1
Manual Deployment

In the AWS Console create and configure an S3 bucket where you will host your app (follow instructions in training materials).
Build and manually upload the MyShop! app to the created S3 bucket. Check if the app is available through the Internet over http://{your-bucket-name}.s3-website-{aws-region}.amazonaws.com .
Create a CloudFront distribution for your app as it was described in training materials. Check your S3 bucket policy changes. Check if the app is available through the Internet over given CloudFront URL.
Make some minor but visible changes in the app, build and upload them to your bucket, and create CloudFront distribution invalidation.
Task 2.2
Automated Deployment

Add and configure serverless and serverless-finch plugin. Add necessary npm script(s) to build and deploy your app from your machine in an automated way. Check if everything works correctly for you. Here's a Demo repo as an example.
NOTE: After uploading an application's build to the S3 bucket you need to manually create a CloudFront invalidation.

Destroy the created AWS infrastructure (S3 bucket and CloudFront distribution) from the previous part and steps. Make sure nothing is left.
Add and configure serverless-single-page-app-plugin as it is implemented in the demo repository. Add necessary npm script(s) to build, upload to your S3 bucket, and invalidate CloudFront cache from your machine in an automated way. Check if everything works fine and all changes appear on the Web.
NOTE: Now that you have this plugin you don’t need to manually create CloudFront invalidations any more.

Task 2.3
Store the links to CloudFront URL and S3-website in README.md file.
Commit all your work to separate branch (e.g. task-2 from the latest master) in your own repository.
Create a pull request to the master branch.
Submit the link to the pull request for crosscheck
Evaluation criteria (70 points for covering all criteria)
S3 bucket has been created and configured properly. The app has been uploaded to the bucket and is available though the Internet. Nothing else has been done. (Link to S3 bucket/website is provided. There is no Pull Request in the YOUR OWN frontend repository.)
In addition to the previous work a CloudFront distribution is created and configured properly and the site is served now with CloudFront and is available through the Internet over CloudFront URL, not S3-website link (due to changes in bucket’s policy...). (Link to CloudFront website is provided. S3-website shows 403 Access Denied error. There is no Pull Request in the YOUR OWN frontend repository.)
Additional (optional) tasks
30 - Serverless-finch and serverless-single-page-app plugins are added and configured. The app can be built and deployed by running npm script command. (Link to CloudFront website is provided. PR with all changes is submitted in the YOUR OWN frontend repository and its link is provided for review.)

### What was done:
Link to S3 bucket/website: http://my-shop-practice.s3-website-eu-west-1.amazonaws.com/
Link to CloudFront website: https://d2wukvticafb1c.cloudfront.net/

S3 bucket has been created and configured properly. The app has been uploaded to the bucket and is available though the Internet. Link to S3 bucket/website is provided.
CloudFront distribution is created and configured properly and the site is served now with CloudFront and is available through the Internet over CloudFront URL. Link to CloudFront website is provided. S3-website shows 403 Access Denied error.

Additional (optional) task:
- Serverless-finch plugin is added and configured. The app can be built by yarn script command. (Link to CloudFront website is provided.  PR with all changes is submitted in my OWN frontend repository and its link is provided for review.)
Not done:
- serverless-single-page-app is not added, automatic deploy fails due to authorisation error.
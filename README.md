# Safe Content Uploads with Amplify and NSFWJS

This project uses [AWS Amplify](https://aws-amplify.github.io/) for file management and [NSFWJS](https://github.com/infinitered/nsfwjs) for content checking.

[![amplifybutton](https://oneclick.amplifyapp.com/button.svg)](https://console.aws.amazon.com/amplify/home#/deploy?repo=https://github.com/kkemple/safe-content-uploads)

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Run locally with the Amplify CLI

1. Install the Amplify CLI (if you get stuck, follow the [getting started](https://aws-amplify.github.io/docs/))

```
npm install -g @aws-amplify/cli
amplify configure
```

1. After the Amplify Console deployment, clone the repo that was just forked in your account

  ```
  git clone git@github.com:<username>/safe-content-uploads.git

  cd safe-content-uploads && yarn
  ```

2. Import the backend environment deployed by the Amplify Console to your repo (the `amplify/team-provider.json` file contains information on all backend environments in your AWS account). The GIF below shows how you to copy the `amplify env import` command from the Amplify Console. 

<img src="https://github.com/aws-samples/create-react-app-auth-amplify/blob/master/src/images/import-backend.gif" width="800"/>

3. Paste this command into your terminal at the root of your repo. You should see the `amplify/team-provider.json` updated with a backend named `amplify`.

  ```
  amplify env import --name amplify --config "{<stack>}" --awsInfo "{<profile>}" --yes

  Successfully added environment from your project
  ```

3. Initialize the Amplify CLI with the `amplify` environment.

  ```
  amplify init
  ? Do you want to use an existing environment? Yes
  ? Choose the environment you would like to use: (Use arrow keys)
  > amplify
  ```

4. Run locally

  ```
  yarn start
  ```

# testkube-actions
Testkube integration with Github Action for k6 test.

This actions workflow:


- Configures the GH action to install Testkube using the Testkube Agent token, organization, and environment ID with Helm.
- Creates and executes the k6 test using `kubeshop/setup-testkube@v1` on the cluster with organization, environment, and API token. Please verify that your token has not expired before running the test.
- Based on the result, the status will be updated in the PR. If the test passes, the merge option will be enabled, and anyone can merge it. However, if the test fails, the merge will not be available—we’ll configure a branch protection rule to prevent the PR from being merged if the run fails.
- The first few lines of the file define a new PR, which triggers all of this.
- Save the workflow file. With this, our basic setup is complete, and we can test.
- All of this happens when a new PR is created which is defined in the first few lines of the file.



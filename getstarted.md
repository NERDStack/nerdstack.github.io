You need Azure.

### :one: Create a new web app

```
nerd install <app_name>
```

*What does this do?*
 1. Clones the sample app (Nerdy Movies) into a new directory
 2. Configures the connection to the back-end DocumentDB data source
 3. Creates and configures the necessary npm scripts

### :two: Run the web app locally

 ```
nerd run
 ```

*What does this do?*
 1. Creates a production build of the web app (`npm run build`)
 2. Runs the platform-appropriate start script (`npm run start-local[-win]`)

### :three: Cleanup the sample app code

*The sample app is an illustration/demo of a running NERD app, but when you are ready to start you app development `nerd cleanup` will remove the unnecessary code from the project*

```
nerd cleanup
```

*What does this do?*
 1. Runs `npm run cleanup` on the project (via [boiler-room-custodian](https://github.com/tstringer/boiler-room-custodian))

### :four: Publish to Azure App Service

```
nerd publish
```

*What does this do?*
 1. Creates the Azure Resource Group (if it doesn't exist)
 2. Creates and configures the Azure Web App in the Resource Group
 3. Ties the web app to a DocumentDB data source (could be the same or different from the dev collection)
 4. Configures local git deployment to the Azure Web App
 5. Configures the upstream repo on the local git repo

> :bulb: Note: this just sets up the Azure resources for hosting and the deployment functionality. It is up to the developer to run `git push azure master` to deploy the web app to Azure App Service

### List Azure regions

```
nerd regions
```

*What does this do?*
 1. Makes a request and displays the Azure regions available

## :bug: Bugs, feature requests, questions

Please open up an [issue on this repo](https://github.com/NERDStack/nerd-cli/issues) for a team member (or community member!) to take action on
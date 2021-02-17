# Basic CRUD App with Go and Gin

This example app shows how to create a API with Go and Gin and display its data with a Vue UI. To follow along step-by-step, [check out the blog post]().

**Prerequisites**: [Go](https://golang.org/doc/install), [Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).

## Getting Started

To install this example application, run the following commands:

```bash
git clone https://github.com/oktadeveloper/okta-go-gin-vue-example.git
cd okta-go-gin-vue-example
cd todo-vue
npm install
npm run build
cd ..
go run main.go
```

This will get a copy of the project install locally. You will need to set up some environment variables before the app will run properly.

To integrate Okta's Identity Platform for user authentication, you'll first need to:

* [Sign up for a free Okta Developer account](https://www.okta.com/developer/signup/)
* You will get a URL similar to `https://dev-123456.oktapreview.com`.
  * Save this URL for later
  * You will also use this URL to login to your Okta account

You will need to create an application in Okta:

* Log in to your Okta account, then navigate to **Applications** and click the **Add Application** button
* Select **Single-Page App** and click **Next**
* Give your application a name (e.g. "Go Gin Web App")
* Change the **Base URI** to `http://localhost:8080/` and the **Login redirect URI** to `http://localhost:8080/login/callback`, then click **Done**
* Save your **Client ID** for later

Now create a file called `.env` in the `todo-vue` directory and add the following variables, replacing the values with your own from the previous steps.

**todo-vue/.env**
```bash
VUE_APP_OKTA_CLIENT_ID={yourClientId}
VUE_APP_OKTA_DOMAIN=https://{yourOktaOrgUrl}
```

Now you can run both the Go/Gin API server and the Vue frontend with the same command:

```bash
go run main.go
```

## Help

Please [raise an issue](https://github.com/oktadeveloper/okta-go-gin-vue-example/issues) if you find a problem with the example application, or visit our [Okta Developer Forums](https://devforum.okta.com/). You can also email [developers@okta.com](mailto:developers@okta.com) if would like to create a support ticket.

## License

Apache 2.0, see [LICENSE](LICENSE).

# App installation

### Prerequisites

* [MongoDB](https://www.mongodb.org/downloads)
* [Node.js 8.0+](http://nodejs.org/)
* Command Line Tools
* **Mac OS X:** [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) \(or **OS X 10.9+**: `xcode-select --install`\)
* **Windows:** [Visual Studio](https://www.visualstudio.com/products/visual-studio-community-vs) OR [Visaul Studio Code](https://code.visualstudio.com/) + [Windows Subsystem for Linux - Ubuntu](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* **Ubuntu** / **Linux Mint:** `sudo apt-get install build-essential`
* **Fedora**: `sudo dnf groupinstall "Development Tools"`
* **OpenSUSE:** `sudo zypper install --type pattern devel_basis`

**Note:** If you are new to Node or Express, I recommend to watch [Node.js and Express 101](https://www.youtube.com/watch?v=BN0JlMZCtNU) screencast by Alex Ford that teaches Node and Express from scratch. Alternatively, here is another great tutorial for complete beginners - [Getting Started With Node.js, Express, MongoDB](http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/).

### Getting Started

The easiest way to get started is to clone the repository:

```text
# Go to you Workspace
cd /path-to-your-workspace

# Get the latest snapshot
git clone --depth=1 git@bitbucket.org:bravebits/ssamt.git

# Change directory
cd ssamt

# Install NPM dependencies
yarn install

# Copy .env.example to .env
cp .env.example .env

# Then simply start your app
yarn start
```

**Warning:** While working with Shopify, it require https, you might need to download [ngrok](https://ngrok.com/). You must start ngrok after starting the project.

```text
# start ngrok to intercept the data exchanged on port 8080
./ngrok http 8080
```

Next, you must use the https url defined by ngrok, for example `https://minhpt.ngrok.io`

Replace it with `BASE_URL` defined in `.env.example` file.

Tried of setting up project? Learn [Docker](https://docs.docker.com/) and then you can do whatever you want with `Dockerfile` and `docker-compose.yml`

### Project Structure

| Name | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **src/config**/passport.js | Passport Local and OAuth strategies, plus login middleware. |
| **src/controllers**/api.js | Controller for /api route and all api examples. |
| **src/controllers**/home.js | Controller for home page \(index\). |
| **src/controllers**/user.js | Controller for user account management. |
| **src/controllers**/shopify.js | Controller for Shopify account management. |
| **src/models**/User.js | Mongoose schema and model for User. |
| **src/models**/Shopify.js | Mongoose schema and model for Shopify. |
| **src/models**/Post.js | Mongoose schema and model for Post. |
| **public**/ | Static assets \(fonts, css, js, img\). |
| **src/views/partials**/flash.pug | Error, info and success flash notifications. |
| **src/views/partials**/header.pug | Navbar partial template. |
| **src/views/partials**/footer.pug | Footer partial template. |
| **src/views**/layout.pug | Base template. |
| **src/views**/home.pug | Home page template. |
| .dockerignore | Folder and files ignored by docker usage. |
| .env.example | Your API keys, tokens, passwords and database URI. |
| .eslintrc | Rules for eslint linter. |
| .gitignore | Folder and files ignored by git. |
| .travis.yml | Configuration files for continue integration. |
| src/app.js | The main application file. |
| src/router.js | The main application Router file. |
| docker-compose.yml | Docker compose configuration file. |
| Dockerfile | Docker configuration file. |
| package.json | NPM dependencies. |
| package-lock.json | Contains exact versions of NPM dependencies in package.json. |

### Integrate with PageFly Core app

```text
# In the Backend core app, let create a folder named pagefly in public
mkdir -p public/pagefly

# Go back to you Workspace
cd /path-to-your-workspace

# Clone the PageFly core repo 
git clone git@bitbucket.org:bravebits/pfapp.git
 
# Change directory
cd pfapp

# Checkout development branch
git checkout development

# Install NPM dependencies
yarn install

# Go to the projects directory (for example: Many Thanks! app)
cd projects/thanks

# Symlink the bundle dist to public/pagefly
ln -s /path-to-your-workspace/ssamt/public/pagefly dist

# Go back project root and then start build the app
yarn dev:thanks

```

### Setting up Shopify development app

Create an Shopify app in [Shopify Partner](https://partners.shopify.com/)

Get the `SHOPIFY_APP_KEY` and `SHOPIFY_APP_SECRET` in App info and update the `.env` file.

Update the `Whitelisted redirection URL(s)` to `https://your-domain.ngrok.com/shopify/auth/callback`

Save and go to `https://your-domain.ngrok.com/shopify/auth?shop=your-shop.myshopify.com`


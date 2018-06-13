# Getting Started

### Prerequisites

* [XAMPP \(Apache + PHP + MySQL\)](https://www.apachefriends.org/index.html)
* [Node.js 8.0+](http://nodejs.org/)
* Command Line Tools
* **Mac OS X:** [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) \(or **OS X 10.9+**: `xcode-select --install`\)
* **Windows:** [Visual Studio](https://www.visualstudio.com/products/visual-studio-community-vs) OR [Visaul Studio Code](https://code.visualstudio.com/) + [Windows Subsystem for Linux - Ubuntu](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* **Ubuntu** / **Linux Mint:** `sudo apt-get install build-essential`
* **Fedora**: `sudo dnf groupinstall "Development Tools"`
* **OpenSUSE:** `sudo zypper install --type pattern devel_basis`



### Getting Started

#### Clone the repository:

```bash
# Go to XAMPP htdocs
cd /path-to-xampp-htdocs

# Clone the SS PageFly backend repo
git clone git@bitbucket.org:bravebits/sspgbldr.git

# Change directory
cd sspgbldr

# Copy conf.php.example to conf.php
cp conf.php.example conf.php
```

Remember to update the _**conf.php**_ file.

#### Install database:

* Turn on your XAMPP:
  * With MacOS, you can search for `manager-osx` and then start the **Apache** and **MySQL**
* Goto: `http://localhost/phpmyadmin`
* Create new Database.
* Import the `schema.sql` in the `database` folder of `sspgbldr`.
* Update database info in `conf.php`
* Update database again:
  * Go to `http://localhost/sspgbldr/database`.
  * Run all the PHP update database file in order of creation date.

#### Create a Shopify Development Store

* Login/Register account in [Shopify Partner](https://partners.shopify.com/).
* Create a development store
* Now you have a development store like: `your-shop-name.myshopify.com`

#### Create a Shopify App

* Login/Register account in [Shopify Partner](https://partners.shopify.com/).
* Create a Shopify App
* Get the App key and update `conf.php` file.
* Update your App URL \(example: `https://localhost/sspgbldr/install.php`\)
* Update your App Whitelisted redirection URL\(s\): `https://localhost/sspgbldr/oauth.php`
* Save the App configuration.
* Go to: `https://localhost/sspgbldr/install.php?shop=you-shop-name.myshopify.com`
* Install the app.

Note: If you facing problem while using `localhost SSL (https)`, go to: `chrome://flags/` and then set the **Allow invalid certificates for resources loaded from localhost** to **Enabled**

Or with alternate way you can using [ngrok](https://ngrok.com/docs).



### Integrate with PageFly Core app

```bash
# In the Backend core app, let create a folder named pagefly in assets
mkdir -p assets/pagefly

# Go to your Workspace
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
cd projects/shopify

# Symlink the bundle dist to public/pagefly
ln -s /path-to-xampp-htdocs/sspgbldr/assets/pagefly dist

# Go back project root and then start build the app
cd ../../

yarn dev:shopify

```




# App installation



### Prerequisites

* [Vagrant + VirtualBox](http://sourabhbajaj.com/mac-setup/Vagrant/README.html)
* [Node.js 8.0+](http://nodejs.org/)
* Command Line Tools
* **Mac OS X:** [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) \(or **OS X 10.9+**: `xcode-select --install`\)
* **Windows:** [Visual Studio](https://www.visualstudio.com/products/visual-studio-community-vs) OR [Visaul Studio Code](https://code.visualstudio.com/) + [Windows Subsystem for Linux - Ubuntu](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* **Ubuntu** / **Linux Mint:** `sudo apt-get install build-essential`
* **Fedora**: `sudo dnf groupinstall "Development Tools"`
* **OpenSUSE:** `sudo zypper install --type pattern devel_basis`



### Getting Started

For Joomla Development, we highly recommended to install via Vagrant by following guide:

#### 

```bash
# Install Vagrant + VirtualBox
brew cask install virtualbox vagrant
# Clone the JSN PageBuilder 3 Repo:
git clone git@bitbucket.org:bravebits/jsnpgbldr2.git

cd jsnpgbldr2
# Start the vagrant for Joomla development
vagrant up
```

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
cd projects/joomla

# Symlink the bundle dist to public/pagefly
ln -s /path-to-jsnpgbldr2/source/joomla/plugins/editors/pagebuilder3/assets/app dist

# Go back project root and then start build the app
cd ../../

yarn dev:joomla
```

#### 

#### Non-Vagrant setup

If you got problem with Vagrant you still can develop JSN PageBuilder 3 with your localhost \(XAMPP\).

Here is the step:

* Firstly, you still need to integrate JSN PageBuilder 3 with PageFly core app follow the previous part
* Secondly, install Joomla into your XAMPP htdocs, link to download: [https://downloads.joomla.org/](https://downloads.joomla.org/)
* Install JSN PageBuilder 3 latest version from [media.bravebits.vn](http://media.bravebits.vn).
* Symlink Source code from `jsnpgbldr2` to your installed Joomla site following example:

```bash
# Delete foldersrm -Rf /path/to/xampp/htdocs/joomla/administrator/components/com_pagebuilder3rm -Rf /path/to/xampp/htdocs/joomla/plugins/editors/pagebuilder3rm -Rf /path/to/xampp/htdocs/joomla/plugins/content/pb3loadmodulerm -Rf /path/to/xampp/htdocs/joomla/plugins/system/pagebuilder3# Symlink foldersln -s /path/to/jsnpgbldr2/source/joomla/admin /path/to/xampp/htdocs/joomla/administrator/components/com_pagebuilder3ln -s /path/to/jsnpgbldr2/source/joomla/plugins/editors/pagebuilder3 /path/to/xampp/htdocs/joomla/plugins/editors/pagebuilder3ln -s /path/to/jsnpgbldr2/source/joomla/plugins/content/pb3loadmodule /path/to/xampp/htdocs/joomla/plugins/content/pb3loadmoduleln -s /path/to/jsnpgbldr2/source/joomla/plugins/system/pagebuilder3 /path/to/xampp/htdocs/joomla/plugins/system/pagebuilder3
```


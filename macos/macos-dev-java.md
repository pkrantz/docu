# Development Java

## Git

Set global identity

```bash
git config --global user.name "Piotr Krantz"
git config --global user.email piotr.krantz@daimlertruck.com
```

## OpenJDK

The `java11` formula is containing the Java 11 LTS version.

```bash
brew install java11
```

To install the latest JDK

```bash
brew install java
```

Homebrew installed the JDK files and directories at

```bash
/usr/local/Cellar/openjdk/
```

and symbolic link `/usr/local/opt/openjdk`.

The java formula is keg-only, which means it is installed in `/usr/local/Cellar` but not linked into places like `/usr/local/bin` or `/Library/Java/JavaVirtualMachines/` (macOS `/usr/bin/java` wrapper).

For macOS `/usr/bin/java` wrapper to find the installed JDK, create a symbolic link at `/Library/Java/JavaVirtualMachines/`.

```bash
sudo ln -sfn /usr/local/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk

java -version
```

List all the JDK versions

```bash
/usr/libexec/java_home -V
or
ls -lsa /Library/Java/JavaVirtualMachines
```

Location of the default JDK

```bash
/usr/libexec/java_home
```

Set the `JAVA_HOME` environment variable in either `~/.bash_profile` or `~/.bashrc`.

```bash
export JAVA_HOME=$(/usr/libexec/java_home)
source ~/.bash_profile
echo $JAVA_HOME
```

## Maven (Manually)

- Download the Maven from `https://archive.apache.org/dist/maven/maven-3`, for example `apache-maven-3.6.1-bin.tar.gz`
- Extract the downloaded .tar.gz file

```bash
pwd
tar -xvzf apache-maven-3.6.1-bin.tar.gz -C ~/tools
```

- Set the `MAVEN_HOME` environment variable in either `~/.bash_profile` or `~/.bashrc` and update the `PATH`

```bash
export MAVEN_HOME=~/apache-maven-3.6.1
export PATH=$PATH:$MAVEN_HOME/bin
source ~/.bash_profile
mvn -version
```

## STS

```bash
brew install --cask springtoolsuite
```

- adapt maven settings config file `settings.xml`

### Install lombok

- find lombok in your project maven directory `Run As -> Java Application`
- specify location
- search for `SpringToolSuit4.init file` and `Install`

## Visual Studion Code

```bash
brew install --cask visual-studio-code
```

Binary 'code' to '/usr/local/bin/code'

## Kubernetes CLI

```bash
brew install kubernetes-cli
kubectl version --client
```

Copy `Polaris` configuration to ~/.kube/config

```bash
mkdir ~/.kube
touch ~/.kube/config
```

## Azure CLI

```bash
brew install azure-cli
```

To sign in and set subscription, use:

```bash
az login
az account list
az account set --subscription Fleetboard_Kosmos_Dev
az account show
```

## Insomnia

```bash
brew install --cask insomnia
```

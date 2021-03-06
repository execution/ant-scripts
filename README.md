# Force.com Migration Tool Sample Config

This repo provides a simple setup of using ANT from your local machine to deploy and retrieve metadata with Salesforce.

## Setup

Follow the instructions here:

https://developer.salesforce.com/docs/atlas.en-us.daas.meta/daas/meta_development.htm

You will need to install ANT (if not already installed), and put the ant-salesforce.jar in the correct location (depending on OS).

Following that, enter your settings in the `build.properties` file, which includes your username, password, URL and other options.

## Commands

### Deploy

`ant deploy`

Put your package.xml and deployment contents into the `deploy` folder, and type `ant deploy` from the command line (from this root directory).

### Retrieve

`ant get`

Put your package.xml of what you want to retrieve, and type `ant get` in your command line. This will retrieve all contents of your package.xml into the retireved folder.

### Retrieve Changeset

`ant getChangeset`

Used to retrieve all contents of a changeset. Put your changeset name in the `build.properties` file and run `ant getChangeset` from the command line.

### Deploy with Test Subset

'ant deploySpecificTests'

Use this to deploy by running just a subset of test methods. Update the `deploySpecificTests` deploy target in the `build.xml` file with the list of tests to run
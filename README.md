## Init
- create a new repo based on this template
  - `gh repo create <project repo> --public --clone --template pwntester/codeql-cs-template`
- copy the zipped database into `databases/` (its better to unzip it in the CS)

## Using packs
- init a new pack `codeql pack init seclab/test`
- add dependencies `codeql pack add codeql/java-all`
- install dependencies `codeql pack install`
- edit query

## Using submodules
- create codeql submodule if needed
  - `git submodule add https://github.com/github/codeql`
  - `git commit -am 'Add CodeQL module'`
  - `git push origin master`
- update codeql submodule if needed:
  - `git submodule init` to initialize your local configuration file 
  - `git submodule update` to fetch all the data from that project and check out the appropriate commit listed in your superproject
- create a `queries` directory
  - create a `qlpack.yml` declaring a `libPathDependencies: codeql/java-all`
  - edit query

## CodeSpaces
-  create the CS
  - `gh cs create --repo <project repo>`
- ssh into the CS
  - `gh cs ssh`

## Cleanup
  - `gh cs delete` to remove and free the CS
  - `gh repo delete` to remove the repo if needed

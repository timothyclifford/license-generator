# Opensauce 🥫

Steps involved in preparing a repository to be open sourced.

## Before you begin

1. [Install Go](https://golang.org/dl/)
1. Install `addlicense` binary to your Go bin (it's a modified version of [this](https://github.com/google/addlicense) to support MPL)
1. `cp ./addlicense $GOPATH/bin/`

## Steps

### 1. Update file exclusions

Update `./exclude` with the file patterns to exclude from the release.

### 2. Copy code

`rsync -av --exclude-from ./exclude SOURCE DESTINATION`

- `SOURCE` - repository path to copy files from
- `DESTINATION` - path to copy files to

### 3. Add license header

`addlicense -l mpl DESTINATION`

- `DESTINATION` - path files were copied to in step 2

### 4. Version

TODO

### 5. Zip

TODO
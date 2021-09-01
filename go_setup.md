
## Remove old package
sudo rm -rfv /usr/local/go

## download and install new package
download: curl -L -o go.pkg https://golang.org/dl/go1.16.2.darwin-amd64.pkg
check: shasum -a 256 go.pkg | grep c3a2e19e49041d835c18a055f34fda1ea56a8599ad12f03a1bfe88d7608f3f5e
(This should print sha256 string back)

run: sudo open go.pkg
remove pkg: rm go.pkg


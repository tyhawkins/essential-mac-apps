# kubectl Configuration

It's probably a good idea to have versioned binaries
of kubectl installed and symlink that to `kubectl`
for the current version of your cluster, since it's a good idea
to match client and server versions up.  Right now, v0.12.8
is the right version, but after you get kubectl installed,
run `kubectl version` and it will tell you your server version.

1. `curl -LO https://storage.googleapis.com/kubernetes-release/release/v0.12.8/bin/linux/amd64/kubectl`
2. `sudo mv kubectl /usr/local/bin/kubectl_0.12.8`
3. `sudo ln -s /usr/local/bin/kubectl_0.12.8 /usr/local/bin/kubectl`

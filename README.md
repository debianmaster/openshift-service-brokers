#### Work in Progress

# on a fresh centos7 machine 
> Install docker,git etc

```sh
curl -LO https://storage.googleapis.com/golang/go1.7.linux-amd64.tar.gz
tar -C /usr/local -xvzf go1.7.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
go version
mkdir $HOME/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export OS_OUTPUT_GOPATH=1
mkdir -p $GOPATH/src/github.com/openshift
cd $GOPATH/src/github.com/openshift
git clone https://github.com/openshift/open-service-broker-sdk
cd open-service-broker-sdk/
make images
> Make sure openshift is running
cd test-scripts
./install-broker.sh
```


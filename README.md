# Kubernetes Autoscaler


This repository contains forke of cluster autoscaler of version 1.12. To fix one bug present in 1.12 till version 1.12.8 The bug is documented in https://github.com/kubernetes/autoscaler/issues/3042#event-3284382539

You can either use the docker image which contain the fix yogeshkunjir/clusterautoscaler:v1.12.8.patch-fix which is of this build or compile below source code or patch offical one and compile using below steps.

## build binary and docker images.

Prerequisites.
Linux with Go and make.
do 
go get https://github.com/kubernetes/kubernetes
go get https://github.com/kubernetes/kubernetes/autoscaler
cd in $GOPATH/src/github.com/kubernetes/autoscaler
make all
you should get binary file use below command to make binary
docker build . -t clusterautoscaler:v1.12.8.patch-fix

## Credit. 
I have made zero changes from my side so all credit to kubernetes author for cluster autoscaler and specail credit for https://github.com/gjtempleton for this patch. 


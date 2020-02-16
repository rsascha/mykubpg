# mykubpg
My Kubernetes Playground

## Start Jenkins and Registry

```
cd build

docker-compose up -d
```

Open: http://localhost:8090/

Registry is running on port 5000.

Sample:
```
docker push localhost:5000/my-image
```

## Jenkins setup

You can use ThinBackup to load my Jenkins setup stored in build/jenkins_backups/

https://wiki.jenkins.io/display/JENKINS/thinBackup

## microk8s

* https://microk8s.io/
* https://microk8s.io/docs/
* https://kubernetes.io/de/docs/home/


## My current setup

```
docker:
Docker version 19.03.0, build aeac949
node:
v12.6.0
npm:
6.9.0
code:
1.36.1
2213894ea0415ee8c85c5eea0d0ff81ecc191529
x64
ng:

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/


Angular CLI: 8.1.2
Node: 12.6.0
OS: linux x64
Angular:
...

Package                      Version
------------------------------------------------------
@angular-devkit/architect    0.801.2
@angular-devkit/core         8.1.2
@angular-devkit/schematics   8.1.2
@schematics/angular          8.1.2
@schematics/update           0.801.2
rxjs                         6.4.0

snap info microk8s
name:      microk8s
summary:   Kubernetes for workstations and appliances
publisher: Canonical*
contact:   https://github.com/ubuntu/microk8s
license:   unset
description: |
  MicroK8s is a small, fast, secure, single node Kubernetes that installs on
  just about any Linux box. Use it for offline development, prototyping,
  testing, or use it on a VM as a small, cheap, reliable k8s for CI/CD. It's
  also a great k8s for appliances - develop your IoT apps for k8s and deploy
  them to MicroK8s on your boxes.
commands:
  - microk8s.config
  - microk8s.ctr
  - microk8s.disable
  - microk8s.enable
  - microk8s.inspect
  - microk8s.istioctl
  - microk8s.kubectl
  - microk8s.linkerd
  - microk8s.reset
  - microk8s.start
  - microk8s.status
  - microk8s.stop
services:
  microk8s.daemon-apiserver:          simple, enabled, active
  microk8s.daemon-apiserver-kicker:   simple, enabled, active
  microk8s.daemon-containerd:         simple, enabled, active
  microk8s.daemon-controller-manager: simple, enabled, active
  microk8s.daemon-etcd:               simple, enabled, active
  microk8s.daemon-kubelet:            simple, enabled, active
  microk8s.daemon-proxy:              simple, enabled, active
  microk8s.daemon-scheduler:          simple, enabled, active
snap-id:      EaXqgt1lyCaxKaQCU349mlodBkDCXRcg
tracking:     stable
refresh-date: today at 18:51 CEST
channels:
  stable:         v1.15.0         2019-06-24 (671) 216MB classic
  candidate:      v1.15.0         2019-06-24 (671) 216MB classic
  beta:           v1.15.0         2019-06-24 (671) 216MB classic
  edge:           v1.15.1         2019-07-18 (711) 192MB classic
  1.16/stable:    --
  1.16/candidate: --
  1.16/beta:      --
  1.16/edge:      v1.16.0-alpha.1 2019-07-19 (714) 190MB classic
  1.15/stable:    v1.15.0         2019-06-24 (670) 216MB classic
  1.15/candidate: v1.15.0         2019-06-24 (670) 216MB classic
  1.15/beta:      v1.15.0         2019-06-24 (670) 216MB classic
  1.15/edge:      v1.15.1         2019-07-18 (710) 192MB classic
  1.14/stable:    v1.14.4         2019-07-18 (687) 217MB classic
  1.14/candidate: v1.14.4         2019-07-12 (687) 217MB classic
  1.14/beta:      v1.14.4         2019-07-12 (687) 217MB classic
  1.14/edge:      v1.14.4         2019-07-08 (687) 217MB classic
  1.13/stable:    v1.13.6         2019-06-06 (581) 237MB classic
  1.13/candidate: v1.13.6         2019-05-09 (581) 237MB classic
  1.13/beta:      v1.13.6         2019-05-09 (581) 237MB classic
  1.13/edge:      v1.13.7         2019-06-06 (625) 244MB classic
  1.12/stable:    v1.12.9         2019-06-06 (612) 259MB classic
  1.12/candidate: v1.12.9         2019-06-04 (612) 259MB classic
  1.12/beta:      v1.12.9         2019-06-04 (612) 259MB classic
  1.12/edge:      v1.12.9         2019-05-28 (612) 259MB classic
  1.11/stable:    v1.11.10        2019-05-10 (557) 258MB classic
  1.11/candidate: v1.11.10        2019-05-02 (557) 258MB classic
  1.11/beta:      v1.11.10        2019-05-02 (557) 258MB classic
  1.11/edge:      v1.11.10        2019-05-01 (557) 258MB classic
  1.10/stable:    v1.10.13        2019-04-22 (546) 222MB classic
  1.10/candidate: v1.10.13        2019-04-22 (546) 222MB classic
  1.10/beta:      v1.10.13        2019-04-22 (546) 222MB classic
  1.10/edge:      v1.10.13        2019-04-22 (546) 222MB classic
installed:        v1.15.0                    (671) 216MB classic
```
*Generated by: `print-my-current-setup.sh`*

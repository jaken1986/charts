# PowerDNS

This is a helm chart for [PowerDNS](http://www.github.com/PowerDNS/) leveraging the [psitrax image](https://hub.docker.com/r/psitrax/powerdns)

## TL;DR;

```shell
$ helm repo add k8s-at-home https://k8s-at-home.com/charts/
$ helm install k8s-at-home/powerdns
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install --name my-release k8s-at-home/powerdns
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release --purge
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration
Read through the powerdns [values.yaml](https://github.com/k8s-at-home/charts/blob/master/charts/powerdns/values.yaml)
file. It has several commented out suggested values.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,
```console
helm install powerdns \
  --set resources.requests.memory="128Mi" \
    k8s-at-home/powerdns
```
Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the
chart. For example,
```console
helm install jackett k8s-at-home/powerdns --values values.yaml 
```

These values will be nested as it is a dependency, for example
```yaml
image:
  tag: ...
```

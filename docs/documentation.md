# Documentation

Most README files are autogenerated. Use [pre-commit](./development.md#pre-commit-hook) or the
tools in [hack/](../hack) to regenerate them.

## Chart Documentation

The [helm-docs](https://github.com/norwoodj/helm-docs) template used to render the charts READMEs
is in [hack/config/helm-docs/README.md.gotmpl](../hack/config/helm-docs/README.md.gotmpl).

Some of the named templates it defines are based on the upcoming 0.14 release of helm-docs and will
be replaced once we update.

How to annotate values is described in the [helm-docs README](https://github.com/norwoodj/helm-docs#valuesyaml-metadata).

You can use `hack/helm-docs.sh` to update the chart READMEs.

## root README and site index

The [gomplate](https://gomplate.ca/) template used to render the root README page is in
[hack/config/update-readme/README.md.gotmpl](../hack/config/update-readme/README.md.gotmpl).

It is used to render both the GitHub README as well as the GitHub Pages index. The differences between
the two output are configured in some YAML files:
* [hack/config/update-readme/readme.yaml](../hack/config/update-readme/readme.yaml)
* [hack/config/update-readme/indexpage.yaml](../hack/config/update-readme/indexpage.yaml)

You can update the README page using `hack/update-readme.md`.
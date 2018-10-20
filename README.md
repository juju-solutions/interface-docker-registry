# Overview

This layer encapsulates the `docker-registry` interface communication
protocol and provides an API for charms on either side of relations using this
interface.

## Usage

In your charm's `layer.yaml`, ensure that `interface:docker-registry` is
included in the `includes` section:

```yaml
includes: ['layer:basic', 'interface:docker-registry']
```

And in your charm's `metadata.yaml`, ensure that a relation endpoint is defined
using the `docker-registry` interface protocol:

```yaml
requires:
  docker-registry:
    interface: docker-registry
```

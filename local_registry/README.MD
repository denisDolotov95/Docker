[Docker Hub](https://hub.docker.com/_/registry)
This image contains an implementation of the OCI Distribution spec. See github.com/opencontainers/distribution-spec for more details about what it is. You can find the full source code in github.com/distribution/distribution.

Run a local registry: Quick Version

```
$ docker run -d -p 5000:5000 --restart always --name registry registry:3
```

Now, use it from within Docker:

```
$ docker pull ubuntu
$ docker tag ubuntu localhost:5000/ubuntu
$ docker push localhost:5000/ubuntu
```

Recommended Reading
The documentation is a good place to learn more about what the registry is, how it works, and how to use it.

Specifically, the section regarding deployment has pointers for more complex use cases than simply running a registry on localhost.
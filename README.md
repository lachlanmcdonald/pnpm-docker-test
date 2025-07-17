# pnpm-docker-test

```sh
docker compose -f .\compose.yml up --build
```

Sample error:

```
 => [internal] load local bake definitions                                                                                              0.0s
 => => reading from stdin 354B                                                                                                          0.0s
 => [internal] load build definition from Dockerfile                                                                                    0.0s
 => => transferring dockerfile: 564B                                                                                                    0.0s
 => resolve image config for docker-image://docker.io/docker/dockerfile:1.7-labs                                                        0.8s
 => [auth] docker/dockerfile:pull token for registry-1.docker.io                                                                        0.0s
 => CACHED docker-image://docker.io/docker/dockerfile:1.7-labs@sha256:b99fecfe00268a8b556fad7d9c37ee25d716ae08a5d7320e6d51c4dd83246894  0.0s
 => [internal] load metadata for docker.io/library/node:24.4.1                                                                          0.5s
 => [auth] library/node:pull token for registry-1.docker.io                                                                             0.0s
 => [internal] load .dockerignore                                                                                                       0.0s
 => => transferring context: 2B                                                                                                         0.0s
 => CANCELED [base 1/4] FROM docker.io/library/node:24.4.1@sha256:601f205b7565b569d3b909a873cc9aa9c6f79b5052a9fe09d73e885760237c4c      2.3s
 => => resolve docker.io/library/node:24.4.1@sha256:601f205b7565b569d3b909a873cc9aa9c6f79b5052a9fe09d73e885760237c4c                    0.1s
 => => sha256:601f205b7565b569d3b909a873cc9aa9c6f79b5052a9fe09d73e885760237c4c 5.14kB / 5.14kB                                          0.0s
 => => sha256:12e348e0dd29bc7d13bfb15b31efd9e1982634a8b9387a4dd3fd45120b1f7a68 2.49kB / 2.49kB                                          0.0s
 => => sha256:2c85757b0aaeaddcd77f5206daeecfdfdfe2c2b3ef576e4eb930ba00e1f2fbf0 6.63kB / 6.63kB                                          0.0s
 => => sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca 17.83MB / 24.02MB                                        2.6s
 => => sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0 16.78MB / 48.49MB                                        2.6s
 => => sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d 13.63MB / 64.40MB                                        2.6s
 => ERROR [internal] load build context                                                                                                 2.1s
 => => transferring context: 20.69MB                                                                                                    2.1s
------
 > [internal] load build context:
------
failed to solve: invalid file request node_modules/.pnpm/color-convert@2.0.1/node_modules/color-name
```

# Usage

Build image:

    $ image=docker.io/f0bec0d/open-webui-time-server
    $ buildah bud -f Dockerfile --layers -t $image .
    $ podman run -p 8000:8000 --rm $image
    $ curl http://localhost:8000/openapi.json

Push to Docker Hub:

    $ buildah login -u f0bec0d docker.io
    $ buildah push $image


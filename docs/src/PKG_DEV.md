

## Docker Environment

**Build the environment**
```sh
docker image build -f ./.config/docker/Dockerfile -t obfacescator-build-img:latest .
```

**Use the environment**
```sh
docker run --rm -it \
    -v $(pwd):/wd
    -w /wd \
    obfacescator-build-img:latest \
    julia
```

**Debugging the `julia` package environment**
```sh
julia> ]
pkg> activate .
pkg> precompile
pkg> <backspace>
julia> err
```

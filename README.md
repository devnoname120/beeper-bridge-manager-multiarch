**Update**: arm64 builds are now officially supported: https://github.com/beeper/bridge-manager/pull/55


# beeper-bridge-manager-multiarch

CI/CD repo for building a multi-arch Container image for Beeper's [Bridge Manager](https://github.com/beeper/bridge-manager). This is to work around a lack of arm support on the primary repo (see [this issue](https://github.com/beeper/bridge-manager/issues/25))

This pipeline runs every 6 hours, 15 minutes past the hour. If a new Beeper bridge-manager image has been published, the pipeline will build a new image on this project.

## Usage

Pulling image:

```
docker pull ghcr.io/holysoles/beeper-bridge-manager-multiarch:latest 
```

For all other usage, please refer to [the original project](https://github.com/beeper/bridge-manager?tab=readme-ov-file#usage).

## License

I make no claims to the underlying source code of this project, this is a project to help facilitate the distribution of the great work that Beeper has done with their Bridge Manager project.

Please review [the Beeper Bridge Manager's LICENSE file](https://github.com/beeper/bridge-manager/blob/main/LICENSE) for additional information. At time of writing, it is licensed under Apache 2.0.

## FAQ

### Why isn't 32-bit Arm (arm/v7) supported?

This is due to a lack of support in a image dependency of the Docker build, [lotticonverter](https://mau.dev/tulir/lottieconverter/container_registry/14). I don't plan to work around that issue at this time, but could if there is interest.

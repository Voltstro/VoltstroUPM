# Voltstro UPM Registry

## What is Voltstro UPM Registry

This service is a [Unity package manager](https://docs.unity3d.com/Manual/Packages.html) custom registry. It is used to provide Voltstro(-Studios) Unity packages. This service also acts as a mirror for [UnityNuGet](https://github.com/xoofx/UnityNuGet).

The service uses [Verdaccio](https://verdaccio.org/) to provide the registry.

To view the online web, simply [go here](https://upm-pkgs.voltstro.dev).

## Setup

### GUI

To use the custom registry:

1. Project Settings **->** Package Manager

2. Add a new scoped registry with the same details below.
![Scoped Registry](media/ScopedRegistry.png)
If you are already using UnityNuGet, and you [don't want to use this registry as a mirror](#using-unitynuget-packages), then exclude `org.nuget` from the scopes.

4. Click 'Apply', you can now use the packages in this registry via the package manager.
![UPM](media/UPM.png)

### Editing `manifest.json`

You can also add this custom registry via editing your project's `manifest.json`, like so:

```json
{
  "dependencies": {
    ...
  },
  "scopedRegistries": [
    {
      "name": "Voltstro UPM",
      "url": "https://upm-pkgs.voltstro.dev",
      "scopes": [
        "dev.voltstro",
        "org.nuget"
      ]
    }
  ]
}

```

### Using UnityNuGet packages

The web view does NOT show UnityNuGet packages, however, they are there. Simply just making requests for the `org.nuget.*` packages will work. Any packages in the [UnityNuGet registry](https://github.com/xoofx/UnityNuGet/blob/master/registry.json) will work. See that project's README for more details.

## TOS

I am not a lawyer, so I will try to keep this simple, also except this part to change over-time.

1. Up-time/Availability

I cannot guarantee a 100% up-time/availability. As stated before this service is hosted for free for anyone to use my packages.

2. Mirroring

If you want to you, you CAN mirror this registry. If you are using this registry in professional/organizational matter, then I suggested that you do.

## Support

We do not provide any professional/enterprise support, we only provide the community [GH Discussions](https://github.com/Voltstro/VoltstroUPM/discussions). Please check/ask there.

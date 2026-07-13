# Cleanflower

Cleanflower is a modern general purpose Java & JVM language decompiler focused on providing the best quality, speed, and usability.
It is a CleanroomMC maintained fork of [Vineflower](https://github.com/Vineflower/vineflower).

Cleanflower's features include:
- Java 21+ support, including records, sealed classes, switch expressions, pattern matching, and more
- Clean code generation and output, with automatic output formatting
- Multithreaded decompilation

Examples of Vineflower/Cleanflower output compared to other decompilers can be found on [the Vineflower website](https://vineflower.org/output-comparison/).

## Use

Cleanflower can be used from the console or as a library. To run Cleanflower from the command line, download the latest release from the [Releases tab](https://github.com/CleanroomMC/Cleanflower/releases).
You can then run Cleanflower with `java -jar cleanflower.jar <arguments> <source> <destination>`.
`<arguments>` is the list of [commandline arguments](https://vineflower.org/usage/) that you want to pass to the decompiler.
`<source>` can be a jar, zip, folder, or class file, and `<destination>` can be a folder, zip, jar, or omitted to print to the console.

To use Cleanflower as a library, you can find distributions on [Cleanroom Maven](https://repo.cleanroommc.com/releases). Cleanflower requires Java 17 or higher to run.
Cleanflower can be added as a dependency in gradle with:
```groovy
repositories {
    maven {
        url 'https://repo.cleanroommc.com/releases'
    }
}

dependencies {
    implementation 'com.cleanroommc:cleanflower:<version>'
}
```

More instructions on how to interface with the decompiler API can be found on [the Vineflower website](https://vineflower.org/usage-code/).

Please report any issues to the [Issues tab!](https://github.com/CleanroomMC/Cleanflower/issues)

### Building
Cleanflower can be built simply with `./gradlew build`.

## Contributing
Contributions are always welcome! When submitting pull requests, please target the latest development branch.
Upstream Vineflower development docs are available on [the Vineflower website](https://vineflower.org/development/).

### Special Thanks
Cleanflower is a fork of Vineflower, which itself is a fork of Jetbrains' Fernflower, MinecraftForge's ForgeFlower, FabricMC's fork of Fernflower. Special thanks to:

* [Stiver](https://blog.jetbrains.com/idea/2024/11/in-memory-of-stiver/), for creating Fernflower
* JetBrains, for maintaining Fernflower
* MinecraftForge Team, for maintaining ForgeFlower
* FabricMC Team, for maintaining Fabric's fork of Fernflower
* CFR, for its large suite of very useful tests

# Maven

A Maven Repository for MrCrayfish's Mods

Simply add the following maven to your `build.gradle`
```gradle
repositories {
    maven {
        name = "MrCrayfish (GitHub)"
        url = "https://maven.pkg.github.com/MrCrayfish/Maven"
    }
}
```

You can then use any published package in your build with the following
```gradle
dependencies {
    // Forge
    compileOnly fb.deobf("com.mrcrayfish:<mod_id>-common-<mc_version>:<mod_version>")
    runtimeOnly fb.deobf("com.mrcrayfish:<mod_id>-forge-<mc_version>:<mod_version>")
    
    // Fabric
    modCompileOnly "com.mrcrayfish:<mod_id>-common-<mc_version>:<mod_version>"
    modRuntimeOnly "com.mrcrayfish:<mod_id>-fabric-<mc_version>:<mod_version>"
}
```

# VH Addon Template for MC Dev Plugin

## Prerequisites
- [MC Development plugin](https://plugins.jetbrains.com/plugin/8327-minecraft-development)

## How to set it up
You can set it up easily in IntelliJ by adding a remote repository in Minecraft Development Settings. Follow these steps:  
1. Go to `File > Settings > Languages & Frameworks > Minecraft Development`
2. Add a remote repository  
3. Click Edit and Set the **Download URL** to:  
   `https://github.com/radimous/vault-hunters-addon-template-for-mcdev/archive/refs/heads/v1.zip`
   
<img width="620" height="406" alt="mcdev-ss" src="https://github.com/user-attachments/assets/ff1e12b2-8eb2-4168-bc7a-20626c49dbd4" />


## How to use

1. Create new project  
   <img width="569" height="770" alt="obrazek" src="https://github.com/user-attachments/assets/2dbc93b0-0a46-4586-ad89-aac7bc39669f" />
2. Wait until project setup finishes
3. Launch the game with `runClient` task or build the jar with `build` task


### MixinExtras
you can uncomment
```
implementation(jarJar("io.github.llamalad7:mixinextras-forge:0.4.1")) {
  jarJar.ranged(it, "[0.4.1,)")
}
 ```
in `build.gradle` to use MixinExtras annotations


## Updating to newer vh version
- tasks mentioned here are under the vh-addon-dev group

1. run the `updateVHJarVersion` task to update to new jar  
2. run the `updateVaultConfigs` to update to new configs  
   2.1. if there are still errors after updating configs try deleting them by using the `deleteVaultConfigs` and running the `updateVaultConfigs` task again


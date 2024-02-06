# GodotProceduralRecoil
Godot port of Gilbert's procedural recoil system for Unity

## Installation
Download `recoil.gd` and import it into your Godot Project.

This script is designed to be used on the parent of the Camera3D node, and the child of the node that is rotated by the mouse input.

![Scene Hierarchy of the player](https://github.com/AceSpectre/GodotProceduralRecoil/blob/main/scene%20heirarchy.png)

In the screenshot above, the `Head` node is rotated by mouse input and `recoil.gd` is attached to the `CameraRecoil` node.

## Usage

### Procdural Recoil Parameters
`Recoil`: Rotation vector added to the target rotation whenever `recoilFire()` is called

`Aim Recoil`: Rotation vector added to the target rotation whenever `recoilFire(true)` is called

`Snappiness`: Rate at which the current rotation lerps to the target rotation

`Return Speed`: Rate at which the target rotation returns to `(0, 0, 0)`

### Functions

`recoilFire(isAiming : bool = false)`
  
- Adds rotation vector to the target rotation, which vector is added is determined by `isAiming`

`setRecoil(newRecoil : Vector3)`
  
- Sets the recoil vector to `newRecoil`

`setAimRecoil(newRecoil : Vector3)`
  
- Sets the aim recoil vector to `newRecoil`

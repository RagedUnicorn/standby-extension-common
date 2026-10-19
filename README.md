# Standby extension: Common

The elements every discipline uses in [Standby](https://github.com/RagedUnicorn/standby):

- **Steel**: popper, mini popper, round plate, square plate.
- **Movers**: swinger, up-and-down, turner. Each takes the board of the stage's discipline from that discipline's extension.
- **Activators**: bear trap, foot pedal, pull handle, push button.
- **The mobile bullet trap**, carrying the target each discipline's extension names.
- **Props**: barrel, barrel pair and stack, tyre stack, table, chair, crate, cone, bag, kettlebell, sandbag, ammo can, rescue dummy, and the handgun, shotgun, rifle and carbine lying on the course.

Standby comes with a release of it. Newer releases reach Standby as updates (Settings, Extensions).

**Viewer:** every element in 2D and 3D, at https://ragedunicorn.github.io/standby-extension-common/

## Changing it

An element is its file `elements/<category>/<id>.json`. An element drawn from files has a drawing `assets/2d/<id>.svg` and a model `assets/3d/<id>.glb`. A board is `boards/<id>.json`. The [extension kit](https://github.com/RagedUnicorn/standby-extension-kit) describes the format, and each file names its schema.

- **See your changes**: `npx https://github.com/RagedUnicorn/standby-extension-kit/releases/download/v0.1.0/standby-extension-kit-0.1.0.tgz view` opens the viewer at http://localhost:4310 and reloads it as you save. To see them in Standby, link this folder: Settings, Extensions, Link a folder.
- **Check them**: `npx https://github.com/RagedUnicorn/standby-extension-kit/releases/download/v0.1.0/standby-extension-kit-0.1.0.tgz validate`, as the CI does.
- **A pull request** gets a preview of the viewer with each changed element before and after, linked in a comment.
- **Ids never change** once stages use them: Standby finds placed elements by id.

## Releasing

Set `version` in extension.json, merge, and push the tag `v<version>`. The workflow releases `<id>-<version>.zip`, which Standby installs, and publishes the viewer. Standby bundles a release by pinning it: `npm run extensions:bump -- <id>` in the standby repository.

## Licence

MIT

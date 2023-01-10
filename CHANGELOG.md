# Changelog

## [0.6.0](https://github.com/bardt/bevy_ecs_ldtk/compare/v0.5.0...v0.6.0) (2023-01-10)


### ⚠ BREAKING CHANGES

* change #[from_entity_instance] to use references ([#149](https://github.com/bardt/bevy_ecs_ldtk/issues/149))
* upgrade to bevy 0.9 ([#138](https://github.com/bardt/bevy_ecs_ldtk/issues/138))
* adjust tile transformations for bevy_ecs_tilemap 0.8 ([#136](https://github.com/bardt/bevy_ecs_ldtk/issues/136))
* upgrade `bevy_ecs_tilemap` dependency to 0.8 ([#134](https://github.com/bardt/bevy_ecs_ldtk/issues/134))
* texture atlas offset for `#[sprite_sheet_bundle...]`

### Features

* add `Respawn` component and rework schedule using it ([7db9394](https://github.com/bardt/bevy_ecs_ldtk/commit/7db939408f0b50fd7b2599e4e1fdb6f6207699f6))
* add LayerMetadata component ([f9be9c7](https://github.com/bardt/bevy_ecs_ldtk/commit/f9be9c70194fb068e9ab9ab35fbfe5bdd520c5d0))
* add LevelSet::from_iid method ([#144](https://github.com/bardt/bevy_ecs_ldtk/issues/144)) ([fb17ae1](https://github.com/bardt/bevy_ecs_ldtk/commit/fb17ae1a2a329c249f01d4728fc585c5550a98c5))
* add respawn flag component ([6c7fea8](https://github.com/bardt/bevy_ecs_ldtk/commit/6c7fea8f5bab57c37039f953a81df6424cb4a423))
* add Respawn to prelude ([c6dfc94](https://github.com/bardt/bevy_ecs_ldtk/commit/c6dfc94d3af4cc2ea587ffc96068c67a2edf4a81))
* add with attribute to LdtkEntity derive ([#128](https://github.com/bardt/bevy_ecs_ldtk/issues/128)) ([18e84be](https://github.com/bardt/bevy_ecs_ldtk/commit/18e84be31a134bae77f3cd1334a5e3b93ca21bc4))
* change #[from_entity_instance] to use references ([#149](https://github.com/bardt/bevy_ecs_ldtk/issues/149)) ([246880f](https://github.com/bardt/bevy_ecs_ldtk/commit/246880f64deeca22e5ab1b733d5afc72f571fc7e))
* implement From&lt;&LayerInstance&gt; for LayerMetadata ([8539846](https://github.com/bardt/bevy_ecs_ldtk/commit/8539846e82bae985e33a522eb2cd3a1ae8da9889))
* insert Name component on ldtk entities, layers, and levels ([33f2b73](https://github.com/bardt/bevy_ecs_ldtk/commit/33f2b737bd6b7b767dda1ff1a3303adb0eb27ef0))
* register types `GridCoords` and `LayerMetadata` ([#146](https://github.com/bardt/bevy_ecs_ldtk/issues/146)) ([ed4a0f9](https://github.com/bardt/bevy_ecs_ldtk/commit/ed4a0f9ae89ed4f709343d097e6652ec905284e5))
* texture atlas offset for `#[sprite_sheet_bundle...]` ([66df968](https://github.com/bardt/bevy_ecs_ldtk/commit/66df96849a8bcd6cdf0f3a52271939a816d98087))
* upgrade `bevy_ecs_tilemap` dependency to 0.8 ([#134](https://github.com/bardt/bevy_ecs_ldtk/issues/134)) ([7d4d1d0](https://github.com/bardt/bevy_ecs_ldtk/commit/7d4d1d0b82692ef60987784019132c31a6f08cf5))
* upgrade to bevy 0.9 ([#138](https://github.com/bardt/bevy_ecs_ldtk/issues/138)) ([048285c](https://github.com/bardt/bevy_ecs_ldtk/commit/048285cff1024b5f319bfb276511f534629b80b3))


### Bug Fixes

* a couple small fixes in tile_makers.rs ([d13be19](https://github.com/bardt/bevy_ecs_ldtk/commit/d13be19d1edf7a78147d37a14c6f801c27141bc3))
* add offset argument to #[sprite_sheet_bundle(...)] macro ([ea6e7a9](https://github.com/bardt/bevy_ecs_ldtk/commit/ea6e7a9618addaa05b5a45ffd2ee839e85a0e27b))
* adjust tile transformations for bevy_ecs_tilemap 0.8 ([#136](https://github.com/bardt/bevy_ecs_ldtk/issues/136)) ([aad0325](https://github.com/bardt/bevy_ecs_ldtk/commit/aad03258f6ba4000676831eed765f792deb0126d))
* do not spawn empty ECS entity for omitted worldly entities ([#122](https://github.com/bardt/bevy_ecs_ldtk/issues/122)) ([a9a0318](https://github.com/bardt/bevy_ecs_ldtk/commit/a9a0318924448613a59203a85669555ef672e266))
* filter out out-of-bounds tiles ([#129](https://github.com/bardt/bevy_ecs_ldtk/issues/129)) ([37dfed0](https://github.com/bardt/bevy_ecs_ldtk/commit/37dfed084f57f35516f636ba5ed0b94042eac63b))
* fire Despawned events for Respawn entities ([5adbf44](https://github.com/bardt/bevy_ecs_ldtk/commit/5adbf44345da8a325c7b579945d49ceaddaeb44f))
* generate new layer_entity within layered_grid_tiles loop ([2060140](https://github.com/bardt/bevy_ecs_ldtk/commit/2060140f8c55454d83f7f7615c9bb705e603023d))
* make choose_levels work for Respawn entities, and apply_level_set work for childless entities ([c41184a](https://github.com/bardt/bevy_ecs_ldtk/commit/c41184aa9615ef5dd3b9eb6449a36c6d1da073d8))
* make level processing system more idempotent ([5d20b0f](https://github.com/bardt/bevy_ecs_ldtk/commit/5d20b0f3337943bc10dd62b3ae2e3850d5a8275b))
* make removing Respawn components from levels more idempotent/conservative ([0ad8d21](https://github.com/bardt/bevy_ecs_ldtk/commit/0ad8d218bd109a3e10264207de5d6a7bcc355b7f))
* make TilemapGridSize nonzero for IntGrid layers w/o AutoTile rules ([e10e0bf](https://github.com/bardt/bevy_ecs_ldtk/commit/e10e0bfda1515c842b011ac2ebde6fc334d6bcc6))
* make world respawning despawn worldly entities as well ([6bfd47f](https://github.com/bardt/bevy_ecs_ldtk/commit/6bfd47feeb642442b4cec060c1e7589c9f8c40b7))
* re-implement SetClearColor::FromEditorBackground functionality ([3f0b787](https://github.com/bardt/bevy_ecs_ldtk/commit/3f0b787df6dc1875d964bdd53dd490b5ff660a73))
* remove a lot of unnecessary work from AssetEvent processing ([1e10b80](https://github.com/bardt/bevy_ecs_ldtk/commit/1e10b8028d5888aae8bf0390dddb05f807170a49))
* remove COPY_SRC creation on modified event ([bfbad90](https://github.com/bardt/bevy_ecs_ldtk/commit/bfbad90a77d8a3b4af4589be2cd001332b025334))
* reorder systems so LevelSelection changes get caught after Update ([438d68f](https://github.com/bardt/bevy_ecs_ldtk/commit/438d68f3904b28c876cb8cdcdc4b0e99c536f4bf))
* resolve de/spawning redundancies between new LDtk entites and new LDtk handles ([056a4e3](https://github.com/bardt/bevy_ecs_ldtk/commit/056a4e3ee9a7c87c6d6b0b91c8e698901684924b))
* set texture atlas offset for sprite_sheet_bundle_from_entity_info ([a79cc05](https://github.com/bardt/bevy_ecs_ldtk/commit/a79cc053d597c4cf2551df58fff4089f61a85c81))
* stop updating level_set every frame ([ecc9207](https://github.com/bardt/bevy_ecs_ldtk/commit/ecc9207afecce48708000a0199707f6474438694))
* update apply_level_set to run whether or not the LevelSet was changed ([89dc9c2](https://github.com/bardt/bevy_ecs_ldtk/commit/89dc9c258600cb91afc0cf3f34f1e4df1cbaedd0))
* update implementation of From&lt;TilePos&gt; for GridCoords to rewrite ([5684669](https://github.com/bardt/bevy_ecs_ldtk/commit/5684669eed3a5856b511db900d4a74da4b697ce8))
* update schedule to work around bevy_ecs_tilemap appropriately ([d829daa](https://github.com/bardt/bevy_ecs_ldtk/commit/d829daa50fb8676eaf5eb565bf35b010c31d9e5f))
* various fixes for rewrite.. ([5684665](https://github.com/bardt/bevy_ecs_ldtk/commit/5684665df7a9c78c754c477caaef4afe4e764324))

## [0.5.0](https://github.com/Trouv/bevy_ecs_ldtk/compare/v0.4.0...v0.5.0) (2022-11-19)


### ⚠ BREAKING CHANGES

* upgrade to bevy 0.9 (#138)
* adjust tile transformations for bevy_ecs_tilemap 0.8 (#136)
* upgrade `bevy_ecs_tilemap` dependency to 0.8 (#134)

### Features

* add with attribute to LdtkEntity derive ([#128](https://github.com/Trouv/bevy_ecs_ldtk/issues/128)) ([18e84be](https://github.com/Trouv/bevy_ecs_ldtk/commit/18e84be31a134bae77f3cd1334a5e3b93ca21bc4))
* insert Name component on ldtk entities, layers, and levels ([33f2b73](https://github.com/Trouv/bevy_ecs_ldtk/commit/33f2b737bd6b7b767dda1ff1a3303adb0eb27ef0))
* upgrade `bevy_ecs_tilemap` dependency to 0.8 ([#134](https://github.com/Trouv/bevy_ecs_ldtk/issues/134)) ([7d4d1d0](https://github.com/Trouv/bevy_ecs_ldtk/commit/7d4d1d0b82692ef60987784019132c31a6f08cf5))
* upgrade to bevy 0.9 ([#138](https://github.com/Trouv/bevy_ecs_ldtk/issues/138)) ([048285c](https://github.com/Trouv/bevy_ecs_ldtk/commit/048285cff1024b5f319bfb276511f534629b80b3))


### Bug Fixes

* adjust tile transformations for bevy_ecs_tilemap 0.8 ([#136](https://github.com/Trouv/bevy_ecs_ldtk/issues/136)) ([aad0325](https://github.com/Trouv/bevy_ecs_ldtk/commit/aad03258f6ba4000676831eed765f792deb0126d))
* do not spawn empty ECS entity for omitted worldly entities ([#122](https://github.com/Trouv/bevy_ecs_ldtk/issues/122)) ([a9a0318](https://github.com/Trouv/bevy_ecs_ldtk/commit/a9a0318924448613a59203a85669555ef672e266))
* filter out out-of-bounds tiles ([#129](https://github.com/Trouv/bevy_ecs_ldtk/issues/129)) ([37dfed0](https://github.com/Trouv/bevy_ecs_ldtk/commit/37dfed084f57f35516f636ba5ed0b94042eac63b))

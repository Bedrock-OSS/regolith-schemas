# regolith-schemas
JSON schemas for Regolith files.

# How does it work
The schemas are stored in separate folders, based on what type of file they
describe (currently only `config` schemas are in the repository). In each
folder, there are files with different versions of schemas named like:
`v1.json`, `v1.1.json`, `v2.json`, etc.

Version `v1` is the stable version of the schema from the `v1` group. In most
cases it will be the same as the latest version that starts with `v1` (e.g.
if `v1.5` exists, but `v1.6` doesn't, `v1` will be the same as `v1.5`).
Regolith always uses the schemas with a single version number.

The first digit is the major version, and it changes only in case of breaking
changes. The second digit is the minor version, and it changes when new
features are added. The third digit (patch) is not used on this repository.
Patches should be applied by updating the schema files.

When you run `regolith init` command to create a new project, Regolith adds
schema to your `config.json`.


## Changelog
### v1.2
- Added the "RpName" and "BpName" name properties to the config.

### v1.1
- Added schema for the "when" property of the fileter
- Added "requirements" property to the "filterDefinitoins"

### v1.0
- Initial release used by Regolith 0.0.18

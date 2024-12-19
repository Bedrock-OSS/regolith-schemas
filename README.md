# regolith-schemas
JSON schemas for Regolith files.

# How does it work. Versions 1.0 to 1.2
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

# How does it work. Versions 1.4 and later
The version of the schema matches the version of Regolith. Version v1 will continue to be updated with the latest schema for Regolith v1.x.x.

## Changelog
### v1.4
- Fixed url issue on the bpName and rpName
- The schema version matches the Regolith version.
- Changed the "export" configuration. The "target" property of the export can be "development", "world", "local", "exact" or "none"
- The properties of the "export" change based on the "target".
- The "development" and "world" targets have new property called "build" that defines which Minecraft build to export to - "education", "standard" or "preview".

### v1.2
- Added the "RpName" and "BpName" name properties to the config.

### v1.1
- Added schema for the "when" property of the fileter
- Added "requirements" property to the "filterDefinitoins"

### v1.0
- Initial release used by Regolith 0.0.18

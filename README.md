# AGOL-Group-Maitenance
A collection of scripts for AGOL group maintenance

## Scripts

### [Bulk Sharing Automation](./bulk_sharing_automation.ipynb)

**Bulk Sharing Automation — Tag-Based Group & Access Level Management**

Automates sharing of AGOL items to groups and sets access levels (`org`, `public`, `group`, `private`) based on configurable tag rules. Includes dry-run preview, validation, and detailed logging.

#### Features

- Tag-based item matching (case-insensitive, all listed tags required)
- Access level management (`org`, `public`, `group`, `private`) separate from group sharing
- Pre-flight configuration validation to catch errors before execution
- Dry-run mode for safe previewing
- Post-run validation confirming items are shared to the correct groups
- Persistent log file at `/arcgis/home/agol_sharing.log`
- Detailed itemised output for both access level and group sharing results

#### How to use

1. Open `bulk_sharing_automation.ipynb` and run the **Connection** cell.
2. Edit the `RULES` list in the **Configuration** cell. Each rule specifies a set of required tags, an optional access level, and target groups.
3. Set `DRY_RUN = True` and run all cells to preview what would change.
4. Review the summary output. When satisfied, set `DRY_RUN = False` and run again to apply.

#### Requirements

- The running account must be a member of all target groups.
- Items must be owned by the running account to be shared.

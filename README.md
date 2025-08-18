# Godot-Editor-Settings-Description
Allow you to set a description on a custom project and editor settings. Useful for making a settings for a plugin.

Currently, godot didn't allow you to add description to a custom project/editor settings. So I made this as a temporary fix.

This is made for an extension of your plugin, so add this to your plugin folder, and the description will be displayed as long as the plugin is in the project.

<img width="1202" height="739" alt="image" src="https://github.com/user-attachments/assets/b7fd1666-1c38-4822-9a49-a511c6753206" />

# Installing
- Download the script and uid file.
- Place them into your plugin folder (e.g. `addons/my_plugin/...`)
# Usage
Preload the script and use the script's `set_editor_setting_desc()` or `set_project_setting_desc()` method to set the description of your custom settings.
### Example:
```gdscript
func _enter_tree() -> void:

	var EditorSettingsDescription = preload("editor_settings_description.gd")
  ## Editor setting description.
	EditorSettingsDescription.set_editor_setting_desc("category/custom_editor_setting","This is a test [b]editor setting[/b] with a description.")
  ## Project setting description.
	EditorSettingsDescription.set_project_setting_desc("category/custom_project_setting","This is a test [b]project setting[/b] with a description.")

```

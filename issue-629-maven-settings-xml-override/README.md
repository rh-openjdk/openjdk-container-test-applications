# Issue #629 - maven_init_var_MAVEN_SETTINGS_XML Override Test

This test application validates that the `maven_init_var_MAVEN_SETTINGS_XML` function can be overridden using the `maven_init_var_MAVEN_SETTINGS_XML_overrides` function.

The custom `.s2i/bin/assemble` script defines the override function before calling the main assemble script, allowing projects to customize the Maven settings.xml location and configuration.

## Expected behavior

- The override function should be called
- Custom settings.xml should be used
- The Maven enforcer plugin should pass because the custom profile is activated

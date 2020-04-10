# Netlify sitemap plugin

Automatically generate a sitemap for your site after it finishes building in Netlify.

## Installation

To install, add the following lines to your `netlify.toml` file:

```toml
[[plugins]]
package = "@netlify/plugin-sitemap"
```

Note: The `[[plugins]]` line is required for each plugin, even if you have other plugins in your `netlify.toml` file already.

## Configuration

Configure the plugin `buildDir`. Default is the `publish` directory from your site build settings.

```toml
[[plugins]]
package = "@netlify/plugin-sitemap"

  [plugins.inputs]
  buildDir = "public"
```

### Excluding files from sitemap

```toml
[[plugins]]
package = "@netlify/plugin-sitemap"

  [plugins.inputs]
  buildDir = "public"
  exclude = [
    # By file Path
    './build-dir/path-to/file.html',
    # By Glob pattern
    '**/**/child-one.html'
  ]
```

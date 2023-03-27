# Changelog

## [0.1.5] - 2023-03-24

### Breaking
- Merged `image_name` and `image_tag` parameters into a single `image_tags` parameter. The new format is `user/app:tag1`.  Multiple tags can now be specified for an image, separated by commas.
This change requires updating your configuration to use the new `image_tags` parameter instead of the deprecated parameters.

### Added
- Added support for the `cache_from` and `cache_to` parameters to enable caching during the build process.

### Removed
- Deprecated `image_name` and `image_tag` parameters in favor of the new `image_tags` parameter. Please update your configuration to use `image_tags` instead.

## [0.1.0 - 2022-06-10 ]
- Initial version

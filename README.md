This is a wrapper class to generate a fully functioning file field type within the ExpressionEngine 3 control panel (or front-end). It uses the native File_ft class to generate all the necessary HTML markup and JavaScript to render a fully functioning file field anywhere in the control panel. Its ideal for usage within 3rd party add-ons that need to save images as form options.
# Usage

$fieldName should be the name of the form field. Can be field_id_1, or foo[something][another_thing]

$fieldValue is the saved value in the database, usually {field_dir_1}something.png
 
$settings is an array of settings required for the native EE File_ft class

```
$fileField = new FileField($fieldName, $fieldValue, $setings);
$options .= '<div class="setting-txt"><em>Image</em></div>' . $fileField->render();
```

## Roadmap

- Add Symfony's OptionsResolver to validate the $settings array
- Add compatibility with the Treasury field type?

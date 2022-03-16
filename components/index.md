---
icon: apps
---

# Components

Here you will find all components in the Garage system.

## Base View

A base view has an id, a type, a value and children.

| Key      | Optional | Example               |
|----------|----------|-----------------------|
| `id`       | Yes      | `$view.login.button`    |
| `type`     | No       | `@view.base.text.title` |
| `value`    | Yes      | `@value.text(Home Page)`             |
| `children` | Yes      | `[ ... ]`               |

## Garage's transformation

You supply a "blueprint" JSON file to Garage, and it will turn this into a "template" file which can be used and interpreted by Garage's client apps.

Garage will auto-generate an `id` for each view (if you have not supplied a user-friendly one already) and populate the file with information so it is usuable by Garage's client apps.

For example, a "blueprint" file that looks like this:
```json
{
  "type": "@view.base.text.title",
  "value": "@value.text($data.screen.event.title)"
}
```
... will be transformed into this:
```json
{
  "id": "$view.47f552975286422eb0e7cb99362ce292",
  "type": "@view.base.text.title",
  "value": "@value.text(Birthday Party!)"
}
```
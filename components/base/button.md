
# Button

`@view.base.button`

A button, which can perform [Actions](/action).

## Example

```json
{
  "id": "$id.home.logoutbutton",
  "type": "@view.base.button",
  "title": "@value.text.account.logout",
  "subtitle": "@value.text($data.user.fullname)",
  "icon": "@icon.account.logout",
  "icon_position": "@style.position.top",
  "block": true,
  "variant": "@style.variant.secondary",
  "actions": [
    {
      "type": "@action.account.logout",
      "on_complete": [
        {
          "type": "@action.navigate",
          "value": "$screen.home"
        }
      ]
    }
  ]
}
```

## Attributes

### Title

```js
title: Value
```

[!ref Value](../value)

### Subtitle

```js
subtitle: Value
```

[!ref Value](../value)

### Icon

```js
icon: Icon
```

[!ref Icon](../icon)

### Icon Position

```js
icon_position: Position
```

[!ref Style position](../style/position)

### Block

```js
block: true | false
```

### Variant

```js
variant: Variant
```

[!ref Style variant](../style/variant)

### Actions

```js
actions: [Action]
```

[!ref Action](../action)
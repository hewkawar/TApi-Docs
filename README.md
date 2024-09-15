# TApi - Tanawat API

# API Reference

### Base URL

```
https://hewkawar.xyz/api
```

or

```
https://tapi.hewkawar.xyz/api
```

## API Versioning

`https://hewkawar.xyz/api/v{version_number}`

| API Version | Status    | Default |
| ----------- | --------- | ------- |
| 1           | Available | ✓       |

# Endpoint

## /discord

Please join the server to get the user data
https://discord.gg/nEfgzJ3dBz

```
GET /discord/users/{user.id}
```

<details>
  <summary>Example Response</summary>

```json
{
  "user": {
    "id": "758681611251744788",
    "bot": false,
    "system": false,
    "flags": 4194560,
    "username": "hewkawar",
    "globalName": "HewkawAr",
    "discriminator": "0",
    "avatar": "429703f71598d7f9f2d851c4005226ca",
    "avatarDecoration": null,
    "createdTimestamp": 1600954191745,
    "defaultAvatarURL": "https://cdn.discordapp.com/embed/avatars/1.png",
    "tag": "hewkawar",
    "avatarURL": "https://cdn.discordapp.com/avatars/758681611251744788/429703f71598d7f9f2d851c4005226ca.webp",
    "displayAvatarURL": "https://cdn.discordapp.com/avatars/758681611251744788/429703f71598d7f9f2d851c4005226ca.webp"
  },
  "presence": "dnd",
  "activities": [
    {
      "name": "Visual Studio Code",
      "type": 0,
      "url": null,
      "details": "📃 TApi-Docs | Bugs 0",
      "state": "📂 README.md:29:12",
      "applicationId": "810516608442695700",
      "timestamps": {
        "start": "2024-09-15T06:03:44.900Z",
        "end": null
      },
      "party": null,
      "syncId": null,
      "assets": {
        "largeText": "Editing a MARKDOWN file",
        "smallText": "Visual Studio Code",
        "largeImage": "mp:external/upBsApcxBvN1KsYpnaBGo2gpIMtYbUQ9ZI90L8HdtgU/https/raw.githubusercontent.com/LeonardSSH/vscord/main/assets/icons/markdown.png",
        "smallImage": "mp:external/Joitre7BBxO-F2IaS7R300AaAcixAvPu3WD1YchRgdc/https/raw.githubusercontent.com/LeonardSSH/vscord/main/assets/icons/vscode.png"
      },
      "flags": 1,
      "emoji": null,
      "buttons": ["Active Label Button 1"],
      "createdTimestamp": 1726381021915
    }
  ]
}
```

</details>

## /images

Free images storage limit 25 MB
Support png, jpg, jpeg, gif, svg, webp

```
POST /images
```

<details>
  <summary>Example Request</summary>

| Field    | Type   | Description     |
| -------- | ------ | --------------- |
| image    | file   | Image to upload |
| owner    | string | Owner ID        |
| filename | string | Filename        |

</details>
<details>
  <summary>Example Response</summary>

```json
{
  "message": "Image uploaded successfully with ID 5",
  "id": 5
}
```

</details>

```
GET /images/{image.id}
```

<details>
  <summary>Example Response</summary>

![Example Image](https://hewkawar.xyz/api/v1/images/5)

</details>

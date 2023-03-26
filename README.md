# Wynem Resource Packs
This repository contains a list of resource packs that will be available through the [Wynem Discord bot](https://wynem.com/) as custom game versions. This means that anyone using the bot will be able to browse its texture files using the bot.

## Submitting Resource Packs
Anyone can submit resource packs to this repository as long as the pack meets certain requirements:
1. You must have full permission from the pack author to put the pack on the bot
2. The pack must be of a high quality, and change a substantial amount of the textures in the game
3. The pack must not be larger than 100MB in size
4. The URL submitted for the pack must hosted on a trusted public website, such as GitHub, CurseForge, Modrinth, MediaFire, etc
5. The pack must not share a name with any past, present, or future Minecraft version

Important: I have the final say of deciding if a pack is on the bot or not, even if it meets all the above criteria.

## How to Submit
1. Go to the `resourcepacks.json` file located in this repository
2. Add your pack to the list, following this format:
```js
"packID": {
  "download": "https://example.com/resourcepack.zip",
  "author": "0123456789"
}
```
3. Create a pull request, and show that you have permission to add the pack (if required)

## JSON format
- Download
  - A direct download link to the ZIP of the resource pack
- Author
  - Your Discord user ID. This will allow you to reload the pack using the `e!reloadpack` command
- Alias
  - An optional field that is an alias ID for the pack
- Name
  - An optional field that will be the name of the pack. By default this is generated from the ID by removing underscores and making it title case

## Download links
The download link that you use must be a direct download to the zip file.
You can use [this link](https://wheregoes.com/trace/20231447411/) to check your download link. The URL should be a link that has a status code of 200. If your download link redirects to a link with 200, just copy the link from after the redirect.
When you have a link that has a status code of 200, confirm it is a direct download by opening a new tab, pasting the link into the address bar, and seeing if it downloads the pack without taking you to a website.

### GitHub
GitHub is the best option for hosting a pack, as it is a dynamic download link. This means that when you update the pack, the link stays the same. For the other services listed below, the link will need to be changed for each update.

<details>
  <summary>Guide</summary>
  <br>
  <ol>
    <li>On the resource pack repository page, click the green code button, right click the <code>Download Zip</code> button, and copy the link.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/github1.png"></li>
  </ol>
</details>

### Modrinth
<details>
  <summary>Guide</summary>
  <br>
  <ol>
    <li>On the resource pack page, copy the download link.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/modrinth1.png"></li>
  </ol>
</details>

### CurseForge
<details>
  <summary>Guide</summary>
  <br>
  <ol>
    <li>To get direct download links on CurseForge, start by right clicking the download button for the file and copying its link.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/curseforge1.png"></li>
    <li>Next, go to a new tab, then open the developer tools there. You can press <code>F12</code> or <code>CTRL+SHIFT+I</code> to do this.</li>
    <li>In the developer tools, switch to the network tab.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/curseforge2.png"></li>
    <li>Paste the copied URL into the address bar and hit enter, you should see some new entries appear in the network tab.</li>
    <li>Select the one that looks like the pack, and you should see the direct download link appear.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/curseforge3.png"></li>
  </ol>
</details>

### Planet Minecraft
This is only for packs that download directly from Planet Minecraft

<details>
  <summary>Guide</summary>
  <br>
  <ol>
    <li>On the resource pack page, open the developer tools. You can press <code>F12</code> or <code>CTRL+SHIFT+I</code> to do this.</li>
    <li>Select the inspect tool, then select the download button using it.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft1.png"><br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft2.png"></li>
    <li>You will be switched to the elements tab. In here, you should have selected, or have nearby, an <code>&lt;a&gt;</code> element with a <code>branded-download</code> class.</li>
    <li>On this element, double click on the <code>target="blank"</code> remove it.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft3.png"><br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft4.png"></li>
    <li>Next, switch to the network tab and clear it.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft5.png"></li>
    <li>Click the download button to download the pack. You should see some new entries appear in the network tab.</li>
    <li>Select the one that looks like the pack, and you should see the direct download link appear.<br><br><img src="https://raw.githubusercontent.com/ewanhowell5195/WynemResourcePacks/main/images/planetminecraft6.png"></li>
  </ol>
</details>

## Updating packs
The process of updating a resource pack depends on what type of download link you used. If the link is a dynamic link, you just need to run the `e!reloadpack` command in Wynem, for example `e!reloadpack f8thful`.

If you used a static link, you will need to first update the link inside this repository, and then after the new link is merged, run the `e!reloadpack` command.

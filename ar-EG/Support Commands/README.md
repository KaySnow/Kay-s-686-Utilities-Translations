## 686 Utiliites: `/support` Commands
Support commands are **single-response** embeds used to quickly answer frequently asked questions or provide help.

⚠️These are *not* interactive guides. If you're looking to create multi-step walkthroughs, contribute to [`/guides`](https://github.com/686-Utilities/686-Utilities-Translations/tree/main/en-GB/Guides) instead.

## How it works:
Each command is stored in an XML file under the Support Commands directory and contains:<br>
A **name**, used as the command keyword.<br>
A **title**, used as the embed heading.<br>
A **description**, for main content (supports markdown).<br>

Optional:
- **Fields** for extra sections.
- **Buttons** for links (max 5). (Link is the only Style supported at the moment).
- **Color** in RGB format (R, G, B).

ℹ️Once live, users can trigger the command using: `/support [name]`.

## 🪄 How to Contribute
1. Fork this repository.
2. Navigate to the Support Commands folder.
3. Add a new .xml file — the filename does not matter, but <Name> must be unique.

Each XML file must contain only one <Command> block.

## 🛠️ Example
```
<Command>
    <Name>Adjusters</Name>
    <Title><![CDATA[Install a Custom Gameconfig, Heap & Packfile Limit Adjuster.]]></Title>
    <Color>89, 0, 255</Color>
    <Description><![CDATA[
**Custom Gameconfig**  
Drag and drop into `mods/update/update.rpf/common/data`.

**Heap Adjuster**  
Drop `.asi` and `.ini` files into your GTA V directory.

**Packfile Limit Adjuster**  
Same as above — `.asi` and `.ini` go in the main folder.
    ]]></Description>
    <Button>
        <Label><![CDATA[Custom Gameconfig]]></Label>
        <Url><![CDATA[https://www.lcpdfr.com/downloads/...]]></Url>
        <Style>Link</Style>
    </Button>
</Command>
```

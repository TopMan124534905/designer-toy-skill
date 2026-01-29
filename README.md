# designer-toy-skill

English | [中文](./README.zh.md)

**Generate designer toy / blind box figure series with consistent character design**

<table>
<tr>
<td width="50%" align="center">
<b>Christmas Cool Boy</b><br/>
Vinyl Plush Style<br/><br/>
<img src="examples/christmas-cool-boy/00-collection-group.png" width="400"/>
</td>
<td width="50%" align="center">
<b>Halloween Bear Felt</b><br/>
Needle Felted Wool Style<br/><br/>
<img src="examples/halloween-bear-felt/00-collection-group-v2.png" width="400"/>
</td>
</tr>
</table>

## Features

| Feature | Description |
|---------|-------------|
| **Character Consistency** | Ensures identical features between group shots and individual shots |
| **Visual Reference Method** | Uses group image as reference to maintain consistency |
| **Pose Diversity** | Sitting, lying, floating poses - not just standing |
| **Rich Scenes** | Complete scene design with lighting, background, atmosphere |
| **Multiple Materials** | Vinyl plush, needle felted wool, and more |

---

## Quick Start

### 1. Install

Copy files to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/designer-toy
cp SKILL.md ~/.claude/skills/designer-toy/
cp -r templates ~/.claude/skills/designer-toy/
```

### 2. Use

In Claude Code, start a conversation:

```
Help me design a Christmas themed blind box series with 5 characters
```

Claude will guide you through:
1. Creating character anchors
2. Designing outfit variations
3. Generating group shot
4. Creating individual shots with visual reference

---

## Workflow

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│  1. Character   │───▶│  2. Design      │───▶│  3. Generate    │
│     Anchor      │    │     Outfits     │    │     Group Shot  │
└─────────────────┘    └─────────────────┘    └────────┬────────┘
                                                       │
┌─────────────────┐    ┌─────────────────┐    ┌────────▼────────┐
│  6. Consistency │◀───│  5. Generate    │◀───│  4. Position    │
│     Check       │    │     Individual  │    │     Mapping     │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

| Phase | Description |
|-------|-------------|
| **Character Anchor** | Lock base features: proportions, face, eyes, skin tone |
| **Design Outfits** | Create outfit anchors with colors, patterns, accessories |
| **Generate Group** | Create collection shot with all characters |
| **Position Mapping** | Document each character's position and features |
| **Generate Individual** | Use group image as visual reference for each shot |
| **Consistency Check** | Verify hair color, outfit, proportions match |

---

## Example: Christmas Cool Boy Series

A vinyl plush style blind box series with 5 characters + 1 hidden edition.

### Group Shot

<p align="center">
<img src="examples/christmas-cool-boy/00-collection-group.png" width="600"/>
</p>

### Individual Shots (with Visual Reference Method)

<table>
<tr>
<td align="center" width="20%">
<img src="examples/christmas-cool-boy/01-christmas-sweater-v2.png" width="150"/><br/>
<b>Christmas Sweater</b><br/>
Standing pose
</td>
<td align="center" width="20%">
<img src="examples/christmas-cool-boy/02-christmas-elf-v2.png" width="150"/><br/>
<b>Christmas Elf</b><br/>
Sitting on gift
</td>
<td align="center" width="20%">
<img src="examples/christmas-cool-boy/03-cozy-winter-v2.png" width="150"/><br/>
<b>Cozy Winter</b><br/>
Snow angel pose
</td>
<td align="center" width="20%">
<img src="examples/christmas-cool-boy/04-gingerbread-v2.png" width="150"/><br/>
<b>Gingerbread</b><br/>
Lying pose
</td>
<td align="center" width="20%">
<img src="examples/christmas-cool-boy/05-starry-snow-night-v2.png" width="150"/><br/>
<b>Starry Night</b><br/>
Floating pose
</td>
</tr>
</table>

---

## Example: Halloween Bear Felt Series

A needle felted wool style blind box series with 5 characters + 1 hidden edition.

### Group Shot

<p align="center">
<img src="examples/halloween-bear-felt/00-collection-group-v2.png" width="600"/>
</p>

### Individual Shots

<table>
<tr>
<td align="center" width="20%">
<img src="examples/halloween-bear-felt/01-pumpkin-cape.png" width="150"/><br/>
<b>Pumpkin Cape</b><br/>
Standing pose
</td>
<td align="center" width="20%">
<img src="examples/halloween-bear-felt/02-little-devil.png" width="150"/><br/>
<b>Little Devil</b><br/>
One-leg balance
</td>
<td align="center" width="20%">
<img src="examples/halloween-bear-felt/03-ghost-cape.png" width="150"/><br/>
<b>Ghost Cape</b><br/>
Floating pose
</td>
<td align="center" width="20%">
<img src="examples/halloween-bear-felt/04-wizard-v2.png" width="150"/><br/>
<b>Wizard</b><br/>
Sitting pose
</td>
<td align="center" width="20%">
<img src="examples/halloween-bear-felt/05-skeleton-hidden.png" width="150"/><br/>
<b>Skeleton</b><br/>
Lying pose
</td>
</tr>
</table>

---

## Key Technique: Visual Reference Method

The core innovation is using the **group image as visual reference** when generating individual shots.

### Why This Matters

| Problem | Solution |
|---------|----------|
| Hair color changes | Reference group image directly |
| Material texture inconsistent | AI sees the exact texture to match |
| Outfit details lost | Position indicator + visual reference |
| Proportions drift | Locked character anchor + visual check |

### How It Works

When generating each individual shot:

1. **Upload group image** to the AI
2. **Specify position**: "Generate the character SECOND from LEFT"
3. **Describe features**: Hair color, outfit, pose
4. **Add scene details**: Background, lighting, atmosphere

---

## Pose Library

| Category | Pose | Keywords |
|----------|------|----------|
| **Sitting** | Cross-legged | `sitting cross-legged on floor` |
| | On object | `sitting on windowsill, legs dangling` |
| **Lying** | On back | `lying on back, snow angel pose` |
| | On stomach | `lying on stomach, chin in hands` |
| | Curled up | `lying on side, curled up, sleepy` |
| **Floating** | Levitation | `floating in air, dreamy` |
| **Dynamic** | One-leg | `standing on one leg, playful` |

---

## Compatibility

| Platform | Status |
|----------|--------|
| Claude Code CLI | ✅ Supported |
| Claude.ai | ✅ Supported (manual prompt) |
| API | ✅ Supported |

---

## License

MIT License - See [LICENSE](LICENSE) for details.

---

<p align="center">
Made with ❤️ for designer toy enthusiasts
</p>

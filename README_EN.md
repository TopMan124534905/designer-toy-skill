# Designer Toy Skill - Blind Box Figure Design Generator

[中文](./README.md) | English

A Pop Mart style blind box figure / designer toy series design generator. This is a Claude Code Skill that helps you design and generate consistent blind box series.

## Core Capabilities

- **Character Consistency**: Ensures character features remain identical between group shots and individual shots (hair color, eyes, proportions)
- **Pose Diversity**: Avoids all-standing poses, provides sitting/lying/floating poses
- **Rich Scenes**: Complete scene design including lighting, background, and atmosphere
- **Visual Reference Method**: Uses group image as reference to ensure individual shots match

## Examples

### Christmas Cool Boy Series

**Group Shot**
![Christmas Group](examples/christmas-cool-boy/00-collection-group.png)

**Individual Shot (generated using group image as visual reference)**
![Christmas Sweater](examples/christmas-cool-boy/01-christmas-sweater-v2.png)

### Halloween Bear Felt Series

**Group Shot**
![Halloween Group](examples/halloween-bear-felt/00-collection-group-v2.png)

**Individual Shot (generated using group image as visual reference)**
![Wizard Bear](examples/halloween-bear-felt/04-wizard-v2.png)

## Installation

Copy `SKILL.md` and `templates/` directory to your Claude Code skills directory:

```bash
# Create skill directory
mkdir -p ~/.claude/skills/designer-toy

# Copy files
cp SKILL.md ~/.claude/skills/designer-toy/
cp -r templates ~/.claude/skills/designer-toy/
```

## Usage

Use the `/designer-toy` command in Claude Code to start the skill, then:

1. Tell Claude the series theme you want to design
2. Claude will help create character anchors and outfit anchors
3. Generate group shot
4. Use group shot as visual reference to generate individual shots
5. Perform consistency check

## Workflow

```
1. Define Character Anchor → 2. Design Series Styles → 3. Generate Group Shot
→ 4. Create Position Mapping → 5. Generate Individual Shots → 6. Consistency Check
```

## Key Technique: Visual Reference Method

When generating individual shots, you **must provide**:
1. **Group Image** - as visual reference
2. **Position Indicator** - specify which character in the group
3. **Text Prompt** - supplementary scene and technical details

This ensures individual shots match the characters in the group image.

## License

MIT

# Designer Toy Skill - 盲盒玩偶设计生成器

[English](./README_EN.md) | 中文

Pop Mart 风格盲盒玩偶/设计师玩具系列设计生成器。这是一个 Claude Code Skill，帮助你设计和生成一致性高的盲盒系列。

## 核心能力

- **角色一致性保障**：确保群像和单人图中角色特征完全一致（发色、眼睛、比例）
- **姿势多样性**：避免全部站姿，提供坐/趴/躺/悬浮等丰富姿势
- **场景丰富度**：包含打光、背景、氛围的完整场景设计
- **视觉参考方法**：使用群像作为参考，确保单人图与群像角色一致

## 示例

### 圣诞小男孩系列 (Christmas Cool Boy)

**群像**
![Christmas Group](examples/christmas-cool-boy/00-collection-group.png)

**单人图（使用群像作为视觉参考生成）**
![Christmas Sweater](examples/christmas-cool-boy/01-christmas-sweater-v2.png)

### 万圣节毛毡熊系列 (Halloween Bear Felt)

**群像**
![Halloween Group](examples/halloween-bear-felt/00-collection-group-v2.png)

**单人图（使用群像作为视觉参考生成）**
![Wizard Bear](examples/halloween-bear-felt/04-wizard-v2.png)

## 安装

将 `SKILL.md` 和 `templates/` 目录复制到你的 Claude Code skills 目录：

```bash
# 创建 skill 目录
mkdir -p ~/.claude/skills/designer-toy

# 复制文件
cp SKILL.md ~/.claude/skills/designer-toy/
cp -r templates ~/.claude/skills/designer-toy/
```

## 使用方法

在 Claude Code 中使用 `/designer-toy` 命令启动技能，然后：

1. 告诉 Claude 你想设计的系列主题
2. Claude 会帮你创建角色锚点和服装锚点
3. 生成群像
4. 使用群像作为视觉参考，逐个生成单人图
5. 进行一致性检查

## 工作流程

```
1. 定义角色锚点 → 2. 设计系列款式 → 3. 生成群像
→ 4. 创建位置映射表 → 5. 逐个生成单人图 → 6. 一致性检查
```

## 关键技术：视觉参考方法

生成单人图时，**必须同时提供**：
1. **群像图片** - 作为视觉参考
2. **位置指示** - 明确指出是群像中的哪个角色
3. **文字 Prompt** - 补充场景和技术细节

这样可以确保单人图与群像中的角色保持一致。

## License

MIT

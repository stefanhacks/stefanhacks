```javascript
export type Stefan = GameDev & TeaHead & DungeonMaster;

export class About extends Me {
  get profile(): Stefan {
    const he: GameDev = {
      mood: '🐙',
      props: ['structure', 'reliance'],
      codes: [TypeScript, CSharp, Python, Lua, sh],
      engines: [Unity, Godot, CocosCreator, Defold],
    };

    const digs: TeaHead & DungeonMaster = {
      drinks: [Leaf.GyokuroAsahi, Blend.AppleBlackberry],
      rolls: [PNP.DnD, PNP.Pathfinder],
    };

    return { ...he, ...digs } as Stefan;
  }

  get workplace(): Record<string, string> {
    return {
      company: 'Play.co',
      position: 'Software Engineer',
      status: 'Onboarding',
    };
  }

  get task(): string {
    const chance = Math.random();

    if (chance < 0.4) return 'coding';
    if (chance < 0.7) return 'hunting monsters';
    if (chance < 0.9) return 'dreaming';
    return 'drinking tea';
  }
}

```

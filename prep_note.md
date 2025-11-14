# Factorio Prep Notes

**Player name:**  Himanshu Raheja
**Game version:** *(from pause overlay)*  : 2.0.69

## Mini‑challenge results

- **Max items/min on one yellow belt:** 900 items/min  
  *Reference: base is 15 items/s total = 900 items/min (7.5/s per lane = 450/min).*

- **Target: 120 green circuits/min**  
  - Iron plates required: **120/min**  
  - Copper plates required (for cables): **180/min**
  - My measured rates (10‑min Production graph):
    - Iron plates: 188/min
    - Copper plates: 180/min
    - Electronic circuits: 120/min

## One bottleneck and the fix
- Bottleneck: The main bus was getting congested because multiple production lines were pulling large quantities of iron and copper simultaneously, slowing down critical circuits production.
- Fix: Split the bus into separate dedicated lanes for high-demand items like iron plates and copper plates, and added priority splitters to ensure essential resources like green circuits always stay supplied.

## One simplification that cleaned up the layout
- Simplification: Replaced multiple small, scattered smelting areas with a single centralized smelting block near the train unloading station. This reduced long conveyor runs, simplified power distribution, and made expansion much easier.
---

## Quick math & ratios (for planning)

- **Yellow belt throughput:** 15 items/s = 900 items/min (total both lanes); 7.5/s = 450/min per lane.
- **Smelting (plates):** Base recipe time 3.2 s/plate.  
  - Stone furnace (speed 1): 60/3.2 = **18.75 plates/min**  
  - Steel/Electric (speed 2): **37.5 plates/min**
- **Green circuits (normal recipe):** 1 iron plate + 3 copper cable → 1 circuit in 0.5 s at speed 1.  
  - Copper cable: 1 copper plate → 2 cable in 0.5 s at speed 1.  
  - For **120 circuits/min**: need **120 iron plates/min** and **180 copper plates/min**.  
  - AM1 (speed 0.5): circuits ≈ 60/min per machine; cables ≈ 120/min per machine. ⇒ **2 circuit AM1 + 3 cable AM1**.  
  - AM2 (speed 0.75): circuits ≈ 90/min; cables ≈ 180/min. ⇒ **2 cable AM2** + **2 circuit AM2 (overprovision)** or throttle to target.

- **Basic oil processing:** 100 crude → 45 petroleum in 5 s ⇒ **9 PG/s per refinery**.  
- **Advanced oil processing:** 100 crude + 50 water → 25 heavy + 45 light + 55 PG (per 5 s). Cracking HO→LO (40→30 in 2 s), LO→PG (30→20 in 2 s).

## Coordinates
- Minimap with grid/coords: open map (M) → enable grid → screenshot.  
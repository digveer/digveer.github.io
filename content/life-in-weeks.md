---
title: "Life in Weeks"
layout: "single"
---

# Life in Weeks

{{< hint info >}}
This visualization shows life as a grid of weeks, where each row represents one year (52 weeks). It's inspired by Gina Trapani's life-in-weeks concept and helps visualize the finite nature of time and the importance of making each week count.
{{< /hint >}}

<div class="life-grid-container">
  <div id="life-grid"></div>
  <div class="legend">
    <div class="legend-item"><span class="legend-box childhood"></span> Childhood (0-12)</div>
    <div class="legend-item"><span class="legend-box teens"></span> Teens (13-19)</div>
    <div class="legend-item"><span class="legend-box early-adult"></span> Early Adulthood (20-29)</div>
    <div class="legend-item"><span class="legend-box thirties"></span> Thirties (30-39)</div>
    <div class="legend-item"><span class="legend-box forties"></span> Forties (40-49)</div>
    <div class="legend-item"><span class="legend-box fifties"></span> Fifties (50-59)</div>
    <div class="legend-item"><span class="legend-box sixties"></span> Sixties (60-69)</div>
    <div class="legend-item"><span class="legend-box seventies"></span> Seventies+ (70+)</div>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const grid = document.getElementById('life-grid');
  const weeksInYear = 52;
  const years = 90; // Assuming a 90-year lifespan
  
  function getPhaseClass(year) {
    if (year < 13) return 'childhood';
    if (year < 20) return 'teens';
    if (year < 30) return 'early-adult';
    if (year < 40) return 'thirties';
    if (year < 50) return 'forties';
    if (year < 60) return 'fifties';
    if (year < 70) return 'sixties';
    return 'seventies';
  }
  
  // Create the grid
  for (let year = 0; year < years; year++) {
    const yearRow = document.createElement('div');
    yearRow.className = 'year-row';
    
    // Add year label
    const yearLabel = document.createElement('div');
    yearLabel.className = 'year-label';
    yearLabel.textContent = year;
    yearRow.appendChild(yearLabel);
    
    // Add weeks
    for (let week = 0; week < weeksInYear; week++) {
      const weekBox = document.createElement('div');
      weekBox.className = `week-box ${getPhaseClass(year)}`;
      weekBox.title = `Year ${year}, Week ${week + 1}`;
      yearRow.appendChild(weekBox);
    }
    
    grid.appendChild(yearRow);
  }
});
</script>

<style>
.life-grid-container {
  overflow-x: auto;
  margin: 20px 0;
  padding: 20px;
  background: var(--body-background);
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

#life-grid {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.year-row {
  display: flex;
  gap: 2px;
  align-items: center;
}

.year-label {
  width: 30px;
  text-align: right;
  padding-right: 10px;
  font-size: 12px;
  color: var(--body-font-color);
}

.week-box {
  width: 8px;
  height: 8px;
  border: 1px solid rgba(0,0,0,0.1);
  transition: all 0.2s;
  opacity: 0.8;
}

.week-box:hover {
  transform: scale(1.2);
  opacity: 1;
  z-index: 1;
}

/* Life phase colors */
.week-box.childhood { background: #FF9999; }
.week-box.teens { background: #FF99CC; }
.week-box.early-adult { background: #CC99FF; }
.week-box.thirties { background: #9999FF; }
.week-box.forties { background: #99CCFF; }
.week-box.fifties { background: #99FFCC; }
.week-box.sixties { background: #CCFF99; }
.week-box.seventies { background: #FFCC99; }

/* Dark mode adjustments */
[data-theme="dark"] .week-box {
  border-color: rgba(255,255,255,0.1);
  opacity: 0.6;
}

[data-theme="dark"] .week-box:hover {
  opacity: 0.9;
}

/* Legend styles */
.legend {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 5px;
  font-size: 14px;
}

.legend-box {
  width: 15px;
  height: 15px;
  border: 1px solid rgba(0,0,0,0.1);
  border-radius: 3px;
}

/* Legend colors */
.legend-box.childhood { background: #FF9999; }
.legend-box.teens { background: #FF99CC; }
.legend-box.early-adult { background: #CC99FF; }
.legend-box.thirties { background: #9999FF; }
.legend-box.forties { background: #99CCFF; }
.legend-box.fifties { background: #99FFCC; }
.legend-box.sixties { background: #CCFF99; }
.legend-box.seventies { background: #FFCC99; }
</style>

## Understanding the Visualization

Each row represents one year of life, broken down into 52 weeks. The colors represent different life phases:

- **Pink** (0-12): Childhood years
- **Rose** (13-19): Teenage years
- **Purple** (20-29): Early adulthood
- **Blue** (30-39): Thirties
- **Light Blue** (40-49): Forties
- **Mint** (50-59): Fifties
- **Light Green** (60-69): Sixties
- **Orange** (70+): Seventies and beyond

The visualization helps to:

1. **Grasp Time's Finite Nature**: Seeing your life laid out in weeks makes the finite nature of time more tangible.
2. **Track Life Progress**: You can visually see where you are in your life journey.
3. **Plan Ahead**: Use this as a tool for long-term planning and goal setting.
4. **Reflect on Past**: Each box represents a week of memories, achievements, and experiences.

## How to Use This Visualization

- Hover over any week to see the specific year and week number
- Use it as a reminder to make each week count
- Consider marking significant life events or milestones
- Use it for planning future goals and aspirations

{{< hint warning >}}
**Remember**  
This visualization isn't meant to create anxiety about time, but rather to inspire mindful living and intentional use of our time.
{{< /hint >}} 
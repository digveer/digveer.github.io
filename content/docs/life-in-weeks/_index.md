---
weight: 6
bookFlatSection: true
title: "Life in Weeks"
---

# Life in Weeks

{{< hint info >}}
This visualization shows life as a grid of weeks, where each row represents one year (52 weeks). It's inspired by Gina Trapani's life-in-weeks concept and helps visualize the finite nature of time and the importance of making each week count.
{{< /hint >}}

<div class="life-grid-container">
  <div id="life-grid"></div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const grid = document.getElementById('life-grid');
  const weeksInYear = 52;
  const years = 90; // Assuming a 90-year lifespan
  
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
      weekBox.className = 'week-box';
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
  background: var(--gray-200);
  border: 1px solid var(--gray-300);
  transition: background-color 0.2s;
}

.week-box:hover {
  background: var(--color-link);
  transform: scale(1.2);
}

/* Dark mode support */
[data-theme="dark"] .week-box {
  background: var(--gray-700);
  border-color: var(--gray-600);
}

[data-theme="dark"] .week-box:hover {
  background: var(--color-link);
}
</style>

## Understanding the Visualization

Each row represents one year of life, broken down into 52 weeks. The visualization helps to:

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
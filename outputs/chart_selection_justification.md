Chart Selection Justification
Overview
This document explains why each chart type was chosen for the dashboard and how the design principles were applied across all views.

Sheet 1 — Sales Trend View (Line Chart)
Chart chosen: Line chart

Why: A line chart is the most natural way to show something changing over time. Sales is a continuous measure that goes up and down month by month, and a line makes it easy to spot trends, peaks, and dips. A bar chart for time series would work but becomes cluttered with many months. The three coloured lines for Furniture, Office Supplies and Technology make it easy to compare categories without confusion.

Design principles applied:

The x-axis is time (months) and the y-axis is sales — this is the standard and expected layout for a trend chart
Each category has its own colour so they are easy to tell apart
The title clearly states what the chart shows
No unnecessary gridlines or decorations were added
Sheet 2 — Regional Performance View (Bar Chart)
Chart chosen: Side by side bar chart

Why: A bar chart is the best choice when comparing values across distinct groups like regions. We have four regions — East, North, South, West — and we want to compare both Sales and Profit for each one. Side by side bars make this comparison direct and easy to read.

Design principles applied:

Bars are sorted by region name so they are easy to find
A reference line was added for average profit so leadership can quickly see which regions are above or below average
Colours are assigned by region so the same colour always means the same region throughout the dashboard
The chart is not overloaded — only Sales and Profit are shown, which are the two most important measures
Sheet 3 — Category Profitability View (Horizontal Bar Chart)
Chart chosen: Horizontal bar chart

Why: Horizontal bars work better than vertical bars when the category names are long — sub-category names like Furnishings, Bookcases, and Accessories are easier to read on the left side of a horizontal bar than rotated at the bottom. This chart also uses colour to show profit level — red for low profit and green for high profit — which adds a second layer of information without adding clutter.

Design principles applied:

Bars are sorted from highest to lowest sales so the most important sub-categories are at the top
Colour encodes profit margin — red means low or negative, green means healthy — making it easy to spot problem areas instantly
Profit margin percentage is labelled directly on each bar so the reader does not have to look at a separate axis
Categories are grouped so Furniture, Office Supplies and Technology are clearly separated
Sheet 4 — Customer Segment View (Grouped Bar Chart)
Chart chosen: Grouped bar chart

Why: We need to compare Sales and Profit across three customer segments and three categories at the same time. A grouped bar chart handles this well by putting related bars next to each other. A pie chart would not work here because we are comparing multiple measures, not parts of a whole.

Design principles applied:

Each segment has a consistent colour throughout the chart
Profit margin labels are shown on bars so the reader gets both volume and profitability in one view
The title is written as a clear business question style heading
Tooltip is set up to give extra detail on hover without cluttering the main view
Sheet 5 — Shipping Performance View (Stacked Bar Chart)
Chart chosen: Stacked bar chart with colour by delivery speed

Why: A stacked bar chart is the right choice when we want to show both the total value and how it is composed. Here we want to see total sales per shipping mode but also understand what proportion of those sales came from fast versus slow deliveries. The colour coding from green (fast) to red (slow) makes the delivery speed story immediately obvious.

Design principles applied:

Colours go from green to red to represent fast to slow — this is intuitive and matches how most people think about performance
The chart shows both Sales and Profit so leadership can see if faster shipping modes are also more profitable
Labels show profit margin so the financial impact of shipping choices is clear
Sheet 6 — Discount vs Profit View (Scatter Plot)
Chart chosen: Scatter plot

Why: A scatter plot is the only chart type that can show the relationship between two numerical measures at the individual order level. Each dot is one order — its position on the x-axis shows the discount rate and its position on the y-axis shows the profit. This makes the negative relationship between discounts and profit immediately visible. A bar chart or line chart could not show this relationship at the order level.

Design principles applied:

A trend line is added to make the direction of the relationship explicit — the downward slope confirms that higher discounts lead to lower profit
A reference line at zero profit clearly separates profitable orders from loss-making ones
Dot size represents sales value so bigger orders stand out
Colours represent category so patterns within each category can be spotted
Sheet 7 — Return Analysis View (Bar Chart)
Chart chosen: Bar chart

Why: Return rate is a simple percentage that needs to be compared across categories and segments. A bar chart is the clearest way to do this. A pie chart would not work because we are not showing parts of a whole — we are comparing separate rates. The reference line for average return rate helps leadership quickly see which groups are above the average and need attention.

Design principles applied:

Return rate is formatted as a percentage with one decimal place — not a raw number — so it is immediately understandable
The average reference line gives context to each bar so leadership knows what is normal
Colours represent regions to add a third dimension of information without adding a separate chart
Labels are shown on bars so the exact percentages are readable without hovering
General Design Principles Applied Across All Charts
Consistent colours: The same colour always means the same thing. For example, the four regions always use the same four colours across every chart where region appears.

Clear titles: Every chart has a plain English title that describes what it shows — not a technical title like "SUM(Sales) by Region" but "Sales and Profit by Region."

Minimal clutter: Only the most important information is shown on each chart. Extra details go in the tooltip so the chart itself stays clean.

Appropriate sorting: Bars are sorted by value where it makes sense so the highest and lowest performers are immediately visible.

No misleading scales: All axes start at zero so bar lengths accurately represent the differences between values. No dual axes were used as these can be misleading.

Useful filters: Filters for Region, Category, Customer Segment, Date, and Ship Mode are applied across all worksheets so any selection updates the entire dashboard at once.
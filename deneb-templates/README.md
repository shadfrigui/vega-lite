# Deneb Templates

A Github Folder for sharing templates for the Power BI custom visual, Deneb.

If you want to experiment with a template, and you don't have a dataset, you can find sample data for each template. Load the sample data into Power BI and import the template.


## Note
Most of the visuals that I create with Vega-Lite/Deneb involve composed views (facet/hconcat/vconcat/repeat); but unfortunately, auto-size is not supported for composed views meaning that end-users need to change the width and height properties of the visuals, which would require other modifications that need to be done. So end-users should be comfortable with editing the "code". 

Also, Deneb doesn't support auto-formatting for columns/measures. For example, if I create a bar-chart template with a currency column on the X-axis with the ```.2s``` D3 format to show values in millions. If an end-user uses a column with another data type, e.g., whole number, percentage, Deneb would still show the ```.2s``` format.

I believe that the usefulness of templates arises from using them by end-users without messing with the code. **So for the reasons above, I've stopped creating templates since March 2022**.  However, if you're comfortable with Vega-Lite/Deneb, take a look at the main repo. Almost for each chart, I've added JSON files for working in the online Vega editor, in VS Code, and in Deneb (```filename-deneb.json```).

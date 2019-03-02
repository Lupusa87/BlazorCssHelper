# Blazor Css Helper


![](https://placehold.it/15/4747d1/000000?text=+) 
If you like my work on blazor and want to see more open sourced demos please support me with donations.
![](https://placehold.it/15/4747d1/000000?text=+) 

[donate via paypal](https://www.paypal.me/VakhtangiAbashidze/50)


![](https://placehold.it/15/00e600/000000?text=+) 
Please send [email](VakhtangiAbashidze@gmail.com) if you consider to **hire me**.
![](https://placehold.it/15/00e600/000000?text=+) 


This css helper is used to generate css classes for components, based on provided settings.

It happens once as settings are received as parameters, styles are generated and can be injected any place in application.

You need to put `<CompCss settings="yourSettings"></CompCss>` anywhere.

It can be injected in html as <style> element or as <link> element with base64 data uri.

example: `<link rel="stylesheet" href="data:text/css;base64,dGR3...I6cn0=" type="text/css">`

This helper class provides fast and easy way to handle conditional styles, you can realize any logic to get desired styles.

Example:
```
  BCssItem _CellRegular = new BCssItem(".CellRegular");
  _CellRegular.Values.Add("border-style", "solid");
  _CellRegular.Values.Add("height", bvgGrid.bvgSettings.RowHeight + "px");
  _CellRegular.Values.Add("background-color", bvgGrid.bvgSettings.CellStyle.BackgroundColor);
  _CellRegular.Values.Add("color", bvgGrid.bvgSettings.CellStyle.ForeColor);
  _CellRegular.Values.Add("border-color", bvgGrid.bvgSettings.CellStyle.BorderColor);
  _CellRegular.Values.Add("border-width", bvgGrid.bvgSettings.CellStyle.BorderWidth + "px;");
  _CellRegular.Values.Add("cursor", "cell");
  blazorCSS.Children.Add(_CellRegular);

```

**Motivation behind this helper**

Instead of giving each element large style attributes we can generate dynamic styles and html elements will have only class attribute (class name).

In case when we can't do static/predefined styles because it's content is depending on provided settings, this helper solves problem.

**In result we get dynamic css**

You can check how it works in only 2 small files [BCss](https://github.com/Lupusa87/BlazorCssHelper/blob/master/BCss)  and [compCss](https://github.com/Lupusa87/BlazorCssHelper/blob/master/CompCSS)

Hope you will find it helpful.

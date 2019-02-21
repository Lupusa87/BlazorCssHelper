# Blazor Css Helper

This css helper is used to generate css classes for component based on provided settings.

It happens once as settings are received as parameters, styles are generated and can be injected any place in application.

You need to put `<CompCss settings="yourSettings"></CompCss>` anywhere.

It can be injected in thml as <style> element or as link element with base64 data uri.

This helper class provides fast and easy way to handle conditional styles.

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

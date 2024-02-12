Dates = 
VAR MinDate = MIN(Sales[Fecha factura])
VAR MaxDate = MAX(Sales[Fecha factura])
RETURN
ADDCOLUMNS
(
    CALENDAR(MinDate, MaxDate), 
    "Dia Semana", WEEKDAY([Date]), 
    "Dia", FORMAT(WEEKDAY([Date]),"dddd"), 
    "Número de Semana",WEEKNUM([Date]),
    "Mes",FORMAT([Date],"MMM"),
    "Mes No.", MONTH([Date])
)

Month offset = 
var currentyear= YEAR(TODAY())
var calendaryear= ('Calendar'[Year])
var yearcalc= (calendaryear-currentyear)*12
var currentmonth= MONTH(TODAY())
var calendarmonth = 'Calendar'[Month]
return yearcalc+(calendarmonth-currentmonth)

# ProphetExample
Learning repo for facebookProphet


This is going to be a simple repo that has data where we can explore it using FbProphet

Hopefully we can find some easy ways to decompose seasonality trends [day of week, week of year etc.]  and underlying growth treds as well as ways to ignore noise.


# Note to get thie library to work we had to fix some import errors
for some reason easter and rd are being imported from the holidays library. This libray has been changed an no longer has those days. To fix this need to add a few lines to the package fbprophet/hdays.py imports

Original Code
from holidays import WEEKEND, HolidayBase, easter, rd

Updated Code
from holidays import WEEKEND, HolidayBase
from dateutil.easter import easter
from dateutil.relativedelta import relativedelta as rd

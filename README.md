# QDateTimeSH
Add support of Solar Hijri date to QDateTime

## Example
```cpp
#include <QApplication>
#include <QDateTimeSH.h>
#include <QMessageBox>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv);

    QDateTimeSH sh = QDateTime::currentDateTime();

    QString format = "امروز ";
    format += "dddd dd MMMM yyyy ";
    format += "ساعت ";
    format += "hh:mm";

    QMessageBox::warning(0, "تاریخ و زمان", sh.toString(format, true));

    return 0;
}
```
# Картинка😊

#include "txlib.h"
int main()
{
int x = 400;
int y = 200;

txCreateWindow(800, 600);
txSetFillColor(TX_BLUE);
txRectangle(0, 0, 800, 600);

txSetFillColor(TX_RED);
txSetColor(TX_BLACK);
txCircle(x, y, 100);

txLine(x-100, y, x+100, y);
txLine(x-100, y+1, x+100, y+1);
txLine(x-100, y-1, x+100, y-1);
txLine(x-100, y+2, x+100, y+2);
txLine(x-100, y-2, x+100, y-2);

txLine(x-100, y, x, y+100);
txLine(x+100, y, x, y+100);
txLine(x, y, x, y+100);
txLine(x, y, x, y-100);
txLine(x-100, y, x, y-100);
txLine(x+100, y, x, y-100);

txSetFillColor(TX_BROWN);
txRectangle(x-50, y+250, x+50, y+320);

txLine(x, y+100, x+50, y+250);
txLine(x, y+100, x-50, y+250);

txSetFillColor(TX_WHITE);
txSetColor(TX_WHITE);

txCircle(150, 100, 20);
txCircle(125, 85, 25);
txCircle(95, 90, 20);

txCircle(750, 100, 20);
txCircle(725, 100, 25);
txCircle(695, 97, 20);

txCircle(143, 200, 20);
txCircle(162, 193, 23);
txCircle(179, 199, 21);

txCircle(720, 210, 21);
txCircle(700,

return 0;
}

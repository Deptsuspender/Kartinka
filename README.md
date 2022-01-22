#include "txlib.h"

void air_ball (int x, int y);
void cloud_1 (int x, int y, int move);
void cloud_2 (int x, int y, int move);
void cloud_3 (int x, int y, int move);
void Karzina (int x, int y);
void Shar (int x, int y);
void Soed_line (int x, int y);

int main ()

{

    txCreateWindow (800, 600);
    txSetFillColor (TX_BLUE);
    txRectangle (0, 0, 800, 600);

    int x = 400;
    int y = 600;

    for (int t=0; t<150; t++)
{
    txClear();

    txSetFillColor (TX_BLUE);
    txRectangle (0, 0, 800, 600);

    y=y-5;
    air_ball(x,y);

    cloud_1(x, 200, 0);
    cloud_2(x, 250, 0);
    cloud_3(x, 320, 0);

    txSleep(60);
}

return 0;
}

void air_ball (int x, int y)
{
    Karzina (x, y);
    Shar (x, y);
    Soed_line (x, y);
}

void cloud_1 (int x, int y, int move)
{
    txSetFillColor (TX_WHITE);
    txSetColor (TX_WHITE);

    txCircle (x-250+5*move, y-100, 20);
    txCircle (x-275+5*move, y-115, 25);
    txCircle (x-305+5*move, y-110, 20);

    txCircle (x+350+5*move, y-100, 20);
    txCircle (x+325+5*move, y-115, 25);
    txCircle (x+295+5*move, y-110, 20);
}

void cloud_2 (int x, int y, int move)
{
    txSetFillColor (TX_WHITE);
    txSetColor (TX_WHITE);

    txCircle (x-250+5*move, y+50, 20);
    txCircle (x-275+5*move, y+65, 25);
    txCircle (x-305+5*move, y+60, 20);

    txCircle (x+320+5*move, y+50, 21);
    txCircle (x+300+5*move, y+65, 23);
    txCircle (x+274+5*move, y+60, 22);
}

void cloud_3 (int x, int y, int move)
{
    txSetFillColor (TX_WHITE);
    txSetColor (TX_WHITE);
    txCircle (x-250+5*move, y+200, 20);
    txCircle (x-275+5*move, y+215, 25);
    txCircle (x-305+5*move, y+210, 20);

    txCircle (x+340+5*move, y+200, 21);
    txCircle (x+317+5*move, y+215, 22);
    txCircle (x+295+5*move, y+210, 22);
}

void Shar (int x, int y)
{
    txSetFillColor (RGB (136, 62, 0));
    txSetColor (TX_BLACK,3);
    txCircle (x, y, 100);

    txLine (x-100, y, x+100, y);

    txLine (x-100, y, x, y+100);
    txLine (x+100, y, x, y+100);
    txLine (x, y, x, y+100);
    txLine (x, y, x, y-100);
    txLine (x-100, y, x, y-100);
    txLine (x+100, y, x, y-100);
}

void Karzina (int x, int y)
{
    txSetColor (TX_BLACK,2);
    txSetFillColor (RGB (51, 23, 0));
    txRectangle (x-50, y+250, x+50, y+320);
}

void Soed_line (int x, int y)
{
    txSetColor (TX_BLACK,3);
    txLine (x, y+100, x+50, y+250);
    txLine (x, y+100, x-50, y+250);
}



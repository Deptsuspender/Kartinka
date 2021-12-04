#include "txlib.h"

void air_ball (int x, int y);
void cloud_1 (int x, int y);
void cloud_2 (int x, int y);
void cloud_3 (int x, int y);
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

for (int i=0; i<70; i++)
{
    txClear();

    txSetFillColor (TX_BLUE);
    txRectangle (0, 0, 800, 600);

    y=y-10;
    air_ball(x,y);

    cloud_1(400,200);
    cloud_2(400,200);
    cloud_3(400,200);

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

void cloud_1 (int x, int y)
{
txSetFillColor (TX_WHITE);
txSetColor (TX_WHITE);

txCircle (x-250, y-100, 20);
txCircle (x-275, y-115, 25);
txCircle (x-305, y-110, 20);

txCircle (x+350, y-100, 20);
txCircle (x+325, y-115, 25);
txCircle (x+295, y-110, 20);
}

void cloud_2 (int x,int y)
{
txSetFillColor (TX_WHITE);
txSetColor (TX_WHITE);

txCircle (x-250, y+50, 20);
txCircle (x-275, y+65, 25);
txCircle (x-305, y+60, 20);

txCircle (x+320, y+50, 21);
txCircle (x+300, y+65, 23);
txCircle (x+274, y+60, 22);
}

void cloud_3 (int x,int y)
{
txSetFillColor (TX_WHITE);
txSetColor (TX_WHITE);
txCircle (x-250, y+200, 20);
txCircle (x-275, y+215, 25);
txCircle (x-305, y+210, 20);

txCircle (x+340, y+200, 21);
txCircle (x+317, y+215, 22);
txCircle (x+295, y+210, 22);
}

void Shar (int x, int y)
{
txSetFillColor (TX_RED);
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
txSetFillColor (TX_BROWN);
txRectangle (x-50, y+250, x+50, y+320);
}

void Soed_line (int x, int y)
{
txSetColor (TX_BLACK,3);
txLine (x, y+100, x+50, y+250);
txLine (x, y+100, x-50, y+250);
}

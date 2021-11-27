#include "txlib.h"

void shar(int x, int y);
void cloud_1(int x, int y);
void cloud_2(int x, int y);
void cloud_3(int x, int y);

int main ()
{
int x = 400;
int y = 200;

txCreateWindow (800, 600);
txSetFillColor (TX_BLUE);
txRectangle (0, 0, 800, 600);

shar(x,y);

cloud_1(x,y);
cloud_2(x,y);
cloud_3(x,y);

return 0;
}

void shar (int x, int y)
{
txSetFillColor (TX_RED);
txSetColor (TX_BLACK);
txCircle (x, y, 100);

txLine (x-100, y, x+100, y);
txLine (x-100, y+1, x+100, y+1);
txLine (x-100, y-1, x+100, y-1);
txLine (x-100, y+2, x+100, y+2);
txLine (x-100, y-2, x+100, y-2);

txLine (x-100, y, x, y+100);
txLine (x+100, y, x, y+100);
txLine (x, y, x, y+100);
txLine (x, y, x, y-100);
txLine (x-100, y, x, y-100);
txLine (x+100, y, x, y-100);

txSetFillColor (TX_BROWN);
txRectangle (x-50, y+250, x+50, y+320);

txLine (x, y+100, x+50, y+250);
txLine (x, y+100, x-50, y+250);
}

void cloud_1 (int x, int y)
{
txSetFillColor (TX_WHITE);
txSetColor (TX_WHITE);

txCircle (x-250, y-100, 20);
txCircle (x-275, y-115, 25);
txCircle (x-305, y-110, 20);

txCircle (x+350, y-100, 20);
txCircle (x+325, y-100, 25);
txCircle (x+295, y-103, 20);
}

void cloud_2(int x,int y)
{
txCircle (x-257, y, 20);
txCircle (x-236, y+7, 23);
txCircle (x-221, y+1, 21);

txCircle (x+320, y+10, 21);
txCircle (x+300, y+10, 23);
txCircle (x+274, y+15, 22);
}

void cloud_3(int x,int y)
{
txCircle (x-230, y+172, 21);
txCircle (x-248, y+179, 22);
txCircle (x-207, y+177, 22);

txCircle (x+340, y+173, 21);
txCircle (x+317, y+169, 22);
txCircle (x+295, y+170, 22);
}

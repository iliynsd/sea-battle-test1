# sea-battle-test1
#include <iostream>
#include "Game.h"
#include "IO.h"
using namespace std;
int main() {
    const int Size = 10;
    char desk1[Size][Size];
    char desk2[Size][Size];
    for (int i = 0; i < Size; ++i) {
        for (int j = 0; j < Size; ++j) {
            desk1[i][j]=' ';
        }
    }
    bool win1, win2;
    int row1;
    int row2;
    int col2;
  int col1;
    int row3;
    int col3;
    int row4;
    int col4;
    int ship4=0;
    int ship3=0;
    int ship2=0;
    int ship1=0;
    int direction;

    cout<<"Locate 4 stage ship\n";
    link1:
       do{ PrintBoard(desk1, Size);
            row1 = InputCoordinate();
            col1 = InputCoordinate();
            cout<<" vertical down(1) gorintol right(2) vertical up(3) gorintol left(4)  ";
            cin>>direction;
            switch(direction)
            {
                case 1:
                   if (row1>6)
                   {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link1;}
                        for (int j = row1; j < row1 + 4; ++j) {
                            desk1[j][col1] = 'H';
                        }

                    break;
                case 2:
                    if (col1>6)

                        {cout<<" uncorrect coordinate, ship is too big"<<endl;
                            goto link1;}

                    for (int j = col1; j < col1+4; ++j) {
                        desk1[row1][j] = 'H';
                    }
                    break;
                case 3:
                    if (row1<3)
                    {cout<<" uncorrect coordinate, ship is too big"<<endl;
                        goto link1;}
                    for (int j = row1-3; j < row1+1; ++j) {
                        desk1[j][col1] = 'H';
                    }
                    break;
                case 4:
                    if (col1<3)

                    {cout<<" uncorrect coordinate, ship is too big"<<endl;
                        goto link1;}

                    for (int j = col1-3; j < col1+1; ++j) {
                        desk1[row1][j] = 'H';
                    }
                    break;
                default: break;
            }

           PrintBoard(desk1, Size);
            ship4++;

        } while (ship4 != 1 );


       ///////////////////////////////////////////////////
    cout<<"Locate 3 stage ships\n";
    link2:
    do{ PrintBoard(desk1, Size);
        row1 = InputCoordinate();
        col1 = InputCoordinate();
        cout<<" vertical down(1) gorintol right(2) vertical up(3) gorintol left(4)  ";
        cin>>direction;
        switch(direction)
        {
            case 1:
                if (row1>7)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link2;}
                for (int j = row1; j < row1 + 3; ++j) {
                    desk1[j][col1] = 'H';
                }

                break;
            case 2:
                if (col1>7)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link2;}

                for (int j = col1; j < col1+3; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            case 3:
                if (row1<2)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link2;}
                for (int j = row1-2; j < row1+1; ++j) {
                    desk1[j][col1] = 'H';
                }
                break;
            case 4:
                if (col1<2)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link2;}

                for (int j = col1-2; j < col1+1; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            default: break;
        }

        PrintBoard(desk1, Size);
        ship3++;

    } while (ship3 != 2 );
    //////////////////////////////////////////////////

    cout<<"Locate 2 stage ships\n";
    link3:
    do{ PrintBoard(desk1, Size);
        row1 = InputCoordinate();
        col1 = InputCoordinate();
        cout<<" vertical down(1) gorintol right(2) vertical up(3) gorintol left(4)  ";
        cin>>direction;
        switch(direction)
        {
            case 1:
                if (row1>8)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link3;}
                for (int j = row1; j < row1 + 2; ++j) {
                    desk1[j][col1] = 'H';
                }

                break;
            case 2:
                if (col1>8)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link3;}

                for (int j = col1; j < col1+2; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            case 3:
                if (row1<1)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link3;}
                for (int j = row1-1; j < row1+1; ++j) {
                    desk1[j][col1] = 'H';
                }
                break;
            case 4:
                if (col1<1)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link3;}

                for (int j = col1-1; j < col1+1; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            default: break;
        }

        PrintBoard(desk1, Size);
        ship2++;

    } while (ship2 != 3 );

/////////////////////////////////////////////

    cout<<"Locate 1 deck ships\n";
    link4:
    do{ PrintBoard(desk1, Size);
        row1 = InputCoordinate();
        col1 = InputCoordinate();
        cout<<" vertical down(1) gorintol right(2) vertical up(3) gorintol left(4)  ";
        cin>>direction;
        switch(direction)
        {
            case 1:
                if (row1>9)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link4;}
                for (int j = row1; j < row1 + 1; ++j) {
                    desk1[j][col1] = 'H';
                }

                break;
            case 2:
                if (col1>9)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link4;}

                for (int j = col1; j < col1+1; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            case 3:
                if (row1<0)
                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link4;}
                for (int j = row1; j < row1+1; ++j) {
                    desk1[j][col1] = 'H';
                }
                break;
            case 4:
                if (col1<0)

                {cout<<" uncorrect coordinate, ship is too big"<<endl;
                    goto link4;}

                for (int j = col1; j < col1+1; ++j) {
                    desk1[row1][j] = 'H';
                }
                break;
            default: break;
        }

        PrintBoard(desk1, Size);
        ship1++;

    } while (ship1 != 4 );




        /*

        winX = WinX(mas);
        if (winX) break;
        cout << "!!! 0 !!!";
        do {
            row = InputCoordinate();
            col = InputCoordinate();
        } while (mas[row][col] != ' ');
        mas[row][col] = '0';
        PrintBoard(mas, Size);
        win0 = Win0(mas);
        if (win0) break;
        draw = Draw(mas, Size);

    } while (!draw);
    if (winX) { cout << " X won" << endl; }
    else if (win0) {
        cout << " 0 won" << endl;
    } else { cout << " Draw" << endl; }*/
}

# MousesFestGame
#include <SFML/Graphics.hpp>
//#include <time.h>
#include <cmath>
#include <ctime>
#include <cstdlib>
#include <Windows.h>
using namespace std;
using namespace sf;

int w = 1920;
int h = 1080;





int main() {
	RenderWindow window(VideoMode(w, h), "Mouses'Fest");

	Texture t1, t2;
	t1.loadFromFile("images/M.jpg");
	t2.loadFromFile("images/red.png");

	Sprite sprite1(t1);
	Sprite sprite2(t2);

	Texture t3;
	t3.loadFromFile("images/map.png");
	Sprite sprite3(t3);

	Texture t4;
	t4.loadFromFile("images/a.jpg");
	Sprite sprite4(t4);

	Texture t5;
	t5.loadFromFile("images/b.jpg");
	Sprite sprite5(t5);

	Texture t6;
	t6.loadFromFile("images/c.jpg");
	Sprite sprite6(t6);

	Texture t7;
	t7.loadFromFile("images/d.jpg");
	Sprite sprite7(t7);

	Texture t8;
	t8.loadFromFile("images/e.jpg");
	Sprite sprite8(t8);

	Texture t9;
	t9.loadFromFile("images/f.jpg");
	Sprite sprite9(t9);


	window.draw(sprite1);
	window.display();



	while (window.isOpen())
	{
		Event e;
		while (window.pollEvent(e)) {
			if (e.type == Event::Closed)
				window.close();
			else if (Keyboard::isKeyPressed(Keyboard::Space))
			{
				window.clear();
				window.draw(sprite3);
				window.display();
			}
			else if (Keyboard::isKeyPressed(Keyboard::Enter))
			{
				int y;
				for (int k = 0; k < 1; k++) {
					window.draw(sprite3);
					window.display();
					for (int a = 0; a < 2; a++) {
						for (int b = 0; b < 2; b++) {
							for (int c = 0; c < 2; c++) {
								for (int d = 0; d < 2; d++) {
									for (int j = 0; j < 2; j++) {

										for (int g = 0; g < 2; g++) {

											for (int i = 0; i < 3; i++) {

												srand(time(0));
												int n = rand() % 6 + 1;
												y = n;
												window.display();
												if (n == 1)
												{
													window.draw(sprite4);
													window.display();
												}
												if (n == 2)
												{
													window.draw(sprite5);
													window.display();
												}
												if (n == 3)
												{
													window.draw(sprite6);
													window.display();
												}
												if (n == 4)
												{
													window.draw(sprite7);
													window.display();
												}
												if (n == 5)
												{
													window.draw(sprite8);
													window.display();
												}
												if (n == 6)
												{
													window.draw(sprite9);
													window.display();
												}


											}
										}

									}
								}
							}
						}
					}
				}






			}
		}
	}
	return 0;
}

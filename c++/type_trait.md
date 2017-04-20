```
/*
 * type_trait.cpp
 *
 *  Created on: 2017年3月24日
 *      Author: wuling
 */

#include <iostream>
using namespace std;


struct dog_tag {};
struct cat_tag {};

class Dog {
public:
	typedef dog_tag type;
};

class Cat {
public:
	typedef cat_tag type;
};


template<typename T>
void Accept(T dog, dog_tag)
{
	cout << "do Dog !" << endl;
}


template<typename T>
void Accept(T cat, cat_tag)
{
	cout << "do Cat !" << endl;
}

template<typename T>
struct AnimalTraits
{
	typedef typename T::type type;
};

template<typename T>
void Accept(T animal)
{
	//Accept(animal, typename T::type());
	Accept(animal, typename AnimalTraits<T>::type());
}

int main()
{
	Cat cat{};
	Dog dog{};

	cout << "accept Cat:" << endl;
	Accept(cat);

	cout << "accept Dog:" << endl;
	Accept(dog);
}
```

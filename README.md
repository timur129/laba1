#ifndef LIST_H
#define LIST_H

class List {
private:
	class Node {
	private:
		int _value;
		Node* _prev;
		Node* _next;
	public:
		Node(int value, Node* prev, Node* next);
		int getValue();
		Node* getPrev();
		Node* getNext();
		void setValue(int value);
		void setPrev(Node* prev);
		void setNext(Node* next);
	};
	Node* _head;
	Node* _tail;
	size_t _size;
public:
	List();
	~List();
	Node* getHead();
	void push_back(int);							//+  добавление в конец списка
	void push_front(int);							//+  добавление в начало списка
	void pop_back();								//+  удаление последнего элемента
	void pop_front();								//+  удаление первого элемента
	void insert(int, size_t);						//+  добавление элемента по индексу (вставка перед элементом, который был ранее доступен по этому индексу)
	int at(size_t);									//+  получение элемента по индексу. Можно сделать типа size_t
	void remove(size_t);							//+  удаление элемента по индексу
	size_t get_size();								//+  получение размера списка
	void print_to_console();						//+  вывод элементов списка в консоль через разделитель, не использовать at
	void clear();									//+  удаление всех элементов списка
	void set(size_t, int);							//+  замена элемента по индексу на передаваемый элемент
	bool isEmpty();									//+  проверка на пустоту списка
	void push_back(List);							//+ вставка другого списка в конец
};

#endif

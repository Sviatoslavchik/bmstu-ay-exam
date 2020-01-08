# BMSTU EXAM по Алгоритмическим языкам (3 семестр)
## Теория(вопросы):
### Вопрос №1 (Двусвязный список: поиск элемента по значению, вставка элемента, удаление элемента. Реализация функции удаления элемента из двусвязного списка. Основные методы std::list. Пример работы с std::list.)
* Определение.
> Двунаправленный (двусвязный) список – это структура данных, состоящая из последовательности элементов, каждый из которых содержит информационную часть и два указателя на соседние элементы.
* Узел двусвязного списка можно представить в виде:
```bash
Struct list{
  int data; // Поле данных
  struct list *next; // Указатель на следующий элемент
  struct list *prev; // Указатель на предыдущий элемент
};
```
* Поиск элемента по значению(Сложность поиска О(n),где n-количество узлов в списке).
```bash
std::find(list.begin(),list.end(),value);
```
* Вставка элемента в список.
1 способ.
```bash
list * addElem(list *lst, int num){
  list *tmp,*p;
  tmp = new struct list * (sizeod(list());
  p = lst ->next;
  lst->next = tmp;
  tmp->data=num;
  tmp->prev=lst;
  if(p!=nullptr)
      p->prev=tmp;
  return tmp;
  }
```
2 способ(при создании).
```bash
list<int> lst = {1,2,3,4,5}; 
```
3 способ(добавление в любую часть контейнера).
```bash
string cpp = "It is easy!";
insert(it,cpp); // it - местоположение(итератор), cpp - значение новой ячейки.
```
* Удаление элемента.
```bash
list<int>a;
a.push_back(1);
a.push_back(2);
a.push_back(3); //1 2 3
a.pop_front(); // 2 3
a.pop_back(); // 2
a.pop_back(); // -
```
* Реализация функции удаления элемента из двусвязного списка.
```bash
list delElem(list *lst){
  list *prev,*next;
  prev = lst -> prev;
  next = lst -> next;
  if(prev!=nullptr) pev->next = lst->next;
  if(next!=nullptr) next->prev = lst->prev;
  delete lst;
  return prev;
}
```
* Основные методы std::list
> clear, insert, erase, push_back, pop_back, push_front, pop_front, swap, size(размер контейнера, работает за О(N)).
* Пример работы с std::list
```bash
list<int> a;
    a.push_back(60);
    a.push_front(29);
    a.push_back(78);
    a.push_front(47);
    for_each(
        a.begin(), 
        a.end(), 
        [](int k){ cout << k<< endl;} // это лямбда-функция
    );
    // 47 29 60 78
```
### Вопрос №2 (Кдасс std::map.Внутренняя реализация map,его основные методы. Сложность поиска, сортировки,удаления элемента, добавления элемента. Пример работы с std::map)




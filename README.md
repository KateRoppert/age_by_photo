# age_by_photo
# Определение возраста покупателей супермаркета по фото с помощью ResNet50
Яндекс.Практикум, Модуль 4, Проект №3

Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:

- Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
- Контролировать добросовестность кассиров при продаже алкоголя.
- 
**Задача:** Построить модель, которая по фотографии определит приблизительный возраст человека. В нашем распоряжении набор фотографий людей с указанием возраста.

**Метрика:** MAE <= 8.

**Общий вывод:**
В задаче была использована модель ResNet50, слои не замораживались, на выходе заменили только один полносвязный слой с одним нейроном, т.к. задача регрессии. Несмотря на то, что данных не очень много, сеть справляется хорошо даже без аугментаций и всего на 5 эпохах. Предположительно, благодаря удачно подобранному значению learning_rate - в ходе решения подбирался только этот параметр. В качестве функции потерь использовали MSE. Модель обучилась довольно быстро.

По условию задачи метрика MAE должна быть не более 8. В использованном решении удалось достичь MAE = 6,8. Следовательно, задача выполнена успешно.

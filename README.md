# NLP-deep-learning-techniques-application-in-context-aware-recommender-systems
В данной работе проводятся попытки опробовать различные техники и приемы из области обработки естественного языка в задачах контекстных рекомендательных систем. Исследование проводится на одном наборе данных, содержащем информацию о заказах посетителей ресторана. Решаемая задача строится следующим образом: генерируются признаки на основе информации из набора данных для обучения базовой модели и затем с помощью нее считаются целевые метрики, далее предпринимаются попытки создать такую новую модель на основании техник из области обработки естественного языка, качество которой по целевым метрикам превысило бы базовую модель, либо использовать подобные техники и приемы для улучшения качества базовой модели. В результате статистически сравниваются различные методы решения задачи рекомендательной системы. В качестве продолжения данного исследования можно опробовать предложенные методы на других наборах данных.

Описание исходных данных находится по [ссылке](https://www.kaggle.com/c/instacart-market-basket-analysis/data) на соревнование на сайте Kaggle.

Все полное описание данной работы находится в файле Master's thesis.pdf, это текст самой магистерской диссертации, лучше скачать его в виде файла pdf для упрощения навигации.

Все промежуточные наборы данных, полученные в результате предобработки, а также модели, полученные в результате обучения не представлены в данном репозитории из-за их большого размера.

Краткое описание ноутбуков приведено ниже:

Prepare_datasets.ipynb - проводится предобработка исходных данных, генерация признаков для обучения базовой модели, генерация выборок для обучения нейросетей.

Word_to_vec.ipynb - проводится обучение алгоритма Word2Vec на последовательностях продуктов, сгенерированных в Prepare_datasets.ipynb, происходит подбор гиперпараметров для базового алгоритма градиентного бустинга, после этого происходит обучение и проверка качества по целевой метрике базовой модели на сгенерированных признаках и на добавочных признаках продуктов, которые получены из модели Word2Vec, а также обучение и проверка качества базовой модели просто на сгенерированных признаках.

Word2Vec_context.ipynb - происходи обучение и проверка качества по целевой метрике базовой модели на сгенерированных признаках и дополнительных признаках контекста, которые представляют собой усредненные вектора продуктов, купленных в предыдущий заказ.

FastText.ipynb - обучение и проверка качества по целевой метрике базовой модели на стандартных признаках и признаках продуктов, полученных из их текстового описания моделью FastText.

ELMO.ipynb - обучение и проверка качества по целевой метрике базовой модели на стандартных признаках и признаках продуктов, полученных из их текстового описания моделью ELMO.

Laser.ipynb - обучение и проверка качества по целевой метрике базовой модели на стандартных признаках и признаках продуктов, полученных из их текстового описания моделью Laser.

BERT.ipynb - обучение и проверка качества по целевой метрике базовой модели на стандартных признаках и признаках продуктов, полученных из их текстового описания моделью BERT.

LSTM_next_sentence_pred.ipynb - обучение и проверка качества сети LSTM в парадигме предсказаниия следующего элемента.

Simple_LSTM.ipynb - обучение и проверка качества сети LSTM в парадигме классификации последовательностей.

LSTM_context.ipynb - добавление к модели из Simple_LSTM.ipynb признаков контекста (день недели, час дня...).

LSTM_Attention.ipynb - добавление к модели Simple_LSTM.ipynb механизма Вниимания.

Seq2Seq.ipynb - обучение Энкодера-Декодера с механизмом Внимания в парадигме перевода одной последовательности в другую.

## Если с первого раза не показывается содержание ноутбуков, нужно нажать кнопку "Reload"


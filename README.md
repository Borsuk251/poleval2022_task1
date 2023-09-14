# PolEval 2022 Task 1: Punctuation prediction from conversational language


Problem predykcji interpunkcji w przypadku Automatycznego Rozpoznawania mowy (Automatic Speech Recognition)  nie jest łatwy do rozwiązania, z uwagi na samą trudność zadania predykcji oraz brak interpunkcji wzorcowej jak w przypadku tekstu pisanego.

Pomysłem na podejście do tego problemu było sprowadzenia go do zadania typu Named Entity Recognition, gdzie dany znak interpunkcyjny odpowiada danej klasie w modelu klasyfikacyjnym. Zastosowaliśmy znane podejście: został wykorzystany odpowiednio duży model językowy, który został douczony na zestawie danych treningowych do zadania. Spośród kilku dostępnych publicznie modeli trenowanych na polskich korpusach, najbardziej obiecujący był HerBERT, oparty na modelu typu BERT.

Użyty został HerBERT w największej dostępnej wersji, sparowany z delikatnym, acz inteligentnym przetwarzaniem otrzymanych wyników. Oczywiście hiperparametry takiej jak wielkość batcha, szybkość czy długość uczenia zostały dostosowane, aby zmaksymalizować generalizację. W końcu, tak przygotowany model pozwolił osiągnąć najwyższy rezultat na referencyjnym zbiorze testowym.



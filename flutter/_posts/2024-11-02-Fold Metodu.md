---

layout: post  
author: fatiharge  
title: Fold Metodu
---

### `fold` Metodu Nedir?
- **Açıklama**: Bir koleksiyondaki elemanları birleştirerek tek bir değer döndürür. Başlangıç değeri ile çalışır.

### Temel Kullanım
```dart
var total = aListOfNumbers.fold(0, (prev, element) {
  return prev + element;
});
```



#### a. String Birleştirme
```dart
var combined = aListOfStrings.fold('', (prev, element) => prev + element);
```

#### b. En Büyük Değeri Bulma
```dart
var max = aListOfNumbers.fold(aListOfNumbers[0], (prev, element) => element > prev ? element : prev);
```

#### c. Koşullu Toplama
```dart
var conditionalTotal = aListOfNumbers.fold(0, (prev, element) => element % 2 == 0 ? prev + element : prev);
```
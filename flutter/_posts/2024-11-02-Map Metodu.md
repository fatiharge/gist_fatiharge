---
layout: post  
author: fatiharge  
title: Map Metodu
---

### `map` Metodu Nedir?
- **Açıklama**: Bir koleksiyondaki her bir elemanı alarak, belirli bir dönüşüm işlemi uygular ve yeni bir koleksiyon döndürür.

### Temel Kullanım
```dart
var squaredList = aListOfNumbers.map((element) {
  return element * element;
}).toList();
```

#### a. String'e Dönüştürme
```dart
var stringList = aListOfNumbers.map((element) => element.toString()).toList();
```

#### b. İlk Harfi Büyük Yapma
```dart
var capitalizedList = aListOfStrings.map((element) => element[0].toUpperCase() + element.substring(1)).toList();
```

#### c. Koşullu Dönüşüm
```dart
var filteredDoubles = aListOfNumbers.map((element) => element * 2).where((element) => element > 10).toList();
```
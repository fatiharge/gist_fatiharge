---
layout: post  
author: fatiharge  
title: Linux Dosya Sahipliğini Değiştirme
---
### Linux `chown` Komutu ile Dosya Sahipliğini Değiştirme

1. **`chown` Komutunun Temel Kullanımı**:  
   `chown` komutu, bir dosyanın veya dizinin sahipliğini değiştirmek için kullanılır. Dosya veya dizin sahibini güncellemek için aşağıdaki gibi bir komut çalıştırabilirsiniz:

   ```sh
   chown [yeni_sahip] dosya_adi
   ```

2. **Sahip ve Grup Belirleme**:
   - Sadece dosya sahibini değiştirmek için:
     ```sh
     chown kullanıcı_adi dosya_adi
     ```
   - Hem dosya sahibi hem de grubunu değiştirmek için:
     ```sh
     chown kullanıcı_adi:grup_adi dosya_adi
     ```

3. **Recursive (Tüm Alt Dizinler İçin) Kullanım**:
   - Bir dizin ve alt dizinleri için sahiplik değiştirmek isterseniz `-R` parametresini ekleyebilirsiniz:
     ```sh
     chown -R kullanıcı_adi:grup_adi dizin_adi
     ```

4. **Örnek Kullanım**:
   - `fatih` kullanıcısına ve `arge` grubuna bir dosyanın sahipliğini vermek için:
     ```sh
     chown fatih:arge ornek_dosya.txt
     ```

## 🧠 Git Cheat Sheet

![image](https://github.com/user-attachments/assets/1821b39f-70be-4943-b193-ff8ac46d5b1f)

---

## 🔍 Git Nedir?

Git, dağıtık mimariye sahip bir versiyon kontrol sistemidir (VCS). Yazılım geliştiricilerin projelerde yaptığı dosya değişikliklerini takip etmelerine, bu değişiklikleri kaydetmelerine veya geri almalarına, dallanmalar (branch) oluşturarak farklı geliştirme akışlarını yönetmelerine olanak tanır.

🎯 Kullanım Alanları

- Proje geçmişini detaylı şekilde izleme
- Yapılan değişiklikleri versiyonlama ve gerektiğinde geri alma
- Takım çalışmasında iş birliğini kolaylaştırma
- Kod tabanı üzerinde paralel geliştirme süreçlerini destekleme

💡 Temel Özellikler

- Dağıtık yapı: Her geliştiricinin kendi yerel deposu vardır
- Yüksek performans: Hızlı ve verimli çalışma sağlar
- Çevrimdışı destek: İnternetsiz ortamlarda da kullanılabilir
- Zengin geçmiş yönetimi: Dosya bazlı ve commit bazlı takip imkânı sunar

---

## ☁️ GitHub Nedir?

GitHub, Git tabanlı yazılım projelerinin bulut ortamında barındırılması, paylaşılması ve üzerinde ekip olarak iş birliği yapılmasını sağlayan bir bulut tabanlı versiyon kontrol ve proje yönetim platformudur.

**🎯 Kullanım Alanları**

- Açık kaynaklı ve kurumsal projelerin merkezi olarak barındırılması
- Pull request ve issue yönetimi üzerinden ekip içi iş akışının sürdürülmesi
- Kod inceleme (code review) ve iş birliği süreçlerinin desteklenmesi

**💡 Temel Özellikler**

- Web tabanlı kullanıcı arayüzü ile kapsamlı proje yönetimi
- CI/CD (Continuous Integration/Deployment) entegrasyonları
- Wiki ve dökümantasyon desteği
- Git işlemlerinin görsel olarak takip edilmesini sağlayan arayüz

---

## 🛠️ Sık Kullanılan Git Komutları

**✅ Temel Git İş Akışı**

```bash
git init                    # Yeni bir Git deposu başlatır
git clone <repo_url>        # Uzak bir depoyu yerel ortama klonlar
git status                  # Çalışma dizinindeki değişiklikleri listeler
git add .                   # Tüm değişiklikleri stage alanına ekler
git commit -m "Mesaj"       # Commit işlemini gerçekleştirir
git push origin main        # Değişiklikleri uzak repoya gönderir
git pull origin main        # Uzak repodan en son değişiklikleri alır
```

**🌿 Branch Yönetimi**

```bash
git branch                     # Tüm branch'leri listeler
git checkout <branch>          # Mevcut bir branch'e geçiş yapar
git checkout -b yeni_branch    # Yeni branch oluşturur ve geçiş yapar
git merge <branch>             # Belirtilen branch'i mevcut branch'e birleştirir
git rebase <branch>            # Mevcut branch'i, hedef branch'in üzerine yeniden düzenler
```

**🔁 Değişiklik Geri Alma**

```bash
git reset --hard <commit_id>    # Geçmişe döner ve değişiklikleri siler
git reset --soft <commit_id>    # Geçmişe döner ama değişiklikleri korur
git revert <commit_id>          # Commit’i geri alır (yeni bir commit olarak)
```

**🔍 Commit Geçmişi ve İnceleme**

```bash
git log                         # Detaylı commit geçmişi
git log --oneline               # Kısa commit listesi
git log --graph --oneline       # Grafiksel commit geçmişi
git diff                        # Değişiklikleri gösterir
git diff main feature/login     # İki branch arasındaki fark
```

**🧪 Hatalı Commit'i Bulma ve Ayıklama**

```bash
git cherry-pick <commit_id>     # Belirli bir commit'i başka bir branch'e uygular
git stash                       # Değişiklikleri geçici olarak saklar
git stash pop                   # Saklanan değişiklikleri geri alır
git reflog                      # Tüm git işlemlerinin geçmişini listeler
```

**🚧 Merge Çatışmaları ve Çözüm**

```bash
git merge feature/api           # Mevcut branch'e başka bir branch'i merge eder
# → Çatışma durumunda:
# 1. Manuel düzeltme
# 2. git add .
# 3. git commit
```

**📚 Rebase Uygulaması**

```bash
git rebase -i HEAD~3            # Son 3 commit’i etkileşimli düzenleme
git rebase --onto main dev      # dev branch'ini main üzerine taşı
```

**🧠 Bonus: Bilinmesi Faydalı Diğer Komutlar**

```bash
git fetch                       # Uzak repodaki değişiklikleri alır (merge yapmaz)
git push --force                # Zorla push işlemi yapar (dikkatli kullanılmalı)
git blame <dosya>               # Satır bazlı değişiklik sorumluluğunu gösterir
git fetch --prune               # Remote’da silinen branch’leri local’de de siler.
```

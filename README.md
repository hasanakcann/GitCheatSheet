## Git Cheat Sheet

![image](https://github.com/user-attachments/assets/1821b39f-70be-4943-b193-ff8ac46d5b1f)

## Git Nedir?

Git, bir versiyon kontrol sistemidir (VCS). Yazılımcıların projelerdeki dosyaları ve kodları zaman içinde takip etmelerini sağlar. Yerel bir sistemde çalışır ve geliştiricilere kod değişikliklerini izleme, geri alma, dallandırma (branching) gibi özellikler sunar.

### Kullanım Alanı:

Git, projelerin yerel bir kopyasında çalışmanıza ve değişiklikleri takip etmenize olanak tanır. Yani, Git yalnızca kodun geçmişini tutar ve yerel sistemdeki veriyi yönetir.

### Özellikler:

Dağıtık versiyon kontrol sistemi olarak, her geliştirici projenin tam bir kopyasını kendi bilgisayarında tutar. Bu sayede çevrimdışı çalışabilir ve her değişiklikte sadece ilgili kısmı commit edebilirsiniz.

- Git: Bir versiyon kontrol aracıdır.

### Commit Example
- git pull origin develop
- git status
- git add .
- git commit -m "fixed"
- git push origin develop

## GitHub Nedir?

GitHub, Git ile çalışan bir platformdur. GitHub, Git'in sunduğu versiyon kontrol özelliklerini, bulut tabanlı bir hizmet olarak sunar. GitHub, kod depolarının internet üzerinde saklanması, paylaşılması ve işbirliği yapılması için kullanılan bir web platformudur.

### Kullanım Alanı:

GitHub, yazılımcıların projelerini depolamak, paylaşmak ve diğer geliştiricilerle işbirliği yapmak için kullanılır. GitHub ayrıca, proje üzerinde yapılacak katkılar (pull request'ler), hata takibi, sürüm yönetimi gibi ek özellikler de sunar.

### Özellikler:

GitHub, kullanıcıların Git reposu oluşturmasına, düzenlemesine ve paylaşmasına olanak tanır. Ayrıca projelerde diğer geliştiricilerle işbirliği yapmayı kolaylaştırır. GitHub üzerinde projelere katkı sağlamak, pull request gönderip almak gibi işlemler yapılabilir.

- GitHub: Git'i kullanarak projeleri barındırabileceğiniz bir platformdur.

## Sık Kullanılan Git Komutları

### Temel Git Komutları

- git init – Yeni bir Git deposu oluşturur.
- git clone <repo_url> – Mevcut bir Git deposunu kopyalar.
- git status – Çalışma dizininin durumunu gösterir.
- git add <dosya_adı> – Belirtilen dosyayı sahneye (staging area) ekler.
- git add . – Tüm değişiklikleri sahneye ekler.
- git commit -m "Açıklama" – Sahneye alınan değişiklikleri depoya kaydeder.
- git commit --amend -m "Yeni açıklama" – Son commit mesajını değiştirir.
- git push origin <branch_adı> – Yerel değişiklikleri uzak depoya gönderir.
- git pull origin <branch_adı> – Uzak depodaki değişiklikleri yerel depoya çeker.
- git fetch – Uzak depodaki değişiklikleri alır ancak birleştirme yapmaz.

### Branch Yönetimi

- git branch – Mevcut dalları (branch) listeler.
- git branch <yeni_branch_adı> – Yeni bir dal oluşturur.
- git branch -d <branch_adı> – Belirtilen dalı siler.
- git branch -D <branch_adı> – Zorla dalı siler.
- git checkout <branch_adı> – Belirtilen dala geçiş yapar.
- git checkout -b <yeni_branch_adı> – Yeni bir dal oluşturur ve ona geçiş yapar.
- git merge <branch_adı> – Belirtilen dalı mevcut dala birleştirir.
- git rebase <branch_adı> – Mevcut dalı başka bir dalın üzerine yeniden düzenler.
- git stash – Geçici olarak değişiklikleri saklar.
- git stash pop – Saklanan değişiklikleri geri yükler.
- git stash list – Saklanan değişiklikleri listeler.
- git stash drop – Belirtilen saklanan değişikliği siler.

### Geçmiş ve Değişiklikleri Yönetme

- git log – Commit geçmişini görüntüler.
- git log --oneline – Commit geçmişini kısa formatta gösterir.
- git log --graph --decorate --oneline – Commit geçmişini dallanma yapısıyla gösterir.
- git diff – Çalışma dizini ile en son commit arasındaki farkları gösterir.
- git diff <branch1> <branch2> – İki dal arasındaki farkları gösterir.
- git reset --hard <commit_id> – Belirtilen commit’e geri döner ve tüm değişiklikleri siler.
- git reset --soft <commit_id> – Belirtilen commit’e geri döner ancak değişiklikleri korur.
- git revert <commit_id> – Belirtilen commit’i geri alır ancak yeni bir commit olarak ekler.

### Uzak Depo Yönetimi

- git remote -v – Uzak depoları listeler.
- git remote add <name> <repo_url> – Yeni bir uzak depo ekler.
- git remote remove <name> – Belirtilen uzak depoyu kaldırır.
- git push --force – Zorla değişiklikleri uzak depoya gönderir.
- git push origin --delete <branch_adı> – Uzak depodaki bir dalı siler.
- git pull --rebase – Uzak depodaki değişiklikleri alır ve mevcut commit’leri yeniden düzenler.

### Etiketleme ve Sürümleme

- git tag <etiket_adı> – Belirtilen commit’e bir etiket ekler.
- git tag -a <etiket_adı> -m "Açıklama" – Açıklamalı bir etiket ekler.
- git tag – Mevcut etiketleri listeler.
- git push origin <etiket_adı> – Etiketi uzak depoya gönderir.
- git push origin --tags – Tüm etiketleri uzak depoya gönderir.
- git tag -d <etiket_adı> – Belirtilen etiketi siler.
- git push origin :refs/tags/<etiket_adı> – Uzak depodaki etiketi siler.

### Alias (Kısayollar) Kullanımı

- git config --global alias.st status – git st komutunu git status olarak çalıştırır.
- git config --global alias.co checkout – git co komutunu git checkout olarak çalıştırır.
- git config --global alias.br branch – git br komutunu git branch olarak çalıştırır.

### Git Hooks (Otomatik İşlemler)

- pre-commit – Commit işleminden önce çalıştırılır.
- commit-msg – Commit mesajı yazıldıktan sonra çalıştırılır.
- pre-push – Push işleminden önce çalıştırılır.

### Git Submodules (Bağımlı Depolar)

- git submodule add <repo_url> – Mevcut projeye bir alt modül ekler.
- git submodule update --init --recursive – Alt modülleri günceller ve başlatır.

### Git Worktrees (Çoklu Çalışma Dizini)

- git worktree add ../yeni_dizin <branch_adı> – Yeni bir çalışma dizini oluşturur.
- git worktree list – Mevcut çalışma dizinlerini listeler.

### Git LFS (Large File Storage)

- git lfs install – Git LFS’i yükler.
- git lfs track "*.psd" – Belirtilen dosya türünü LFS ile takip eder.

### Git Bisect (Hatalı Commit’i Bulma)

- git bisect start – Bisect işlemini başlatır.
- git bisect bad – Hatalı commit’i işaretler.
- git bisect good – Çalışan commit’i işaretler.

### Git Reflog (Silinen Commit’leri Geri Getirme)

- git reflog – Tüm Git işlemlerinin geçmişini gösterir.
- git reset --hard HEAD@{3} – 3 işlem önceki duruma geri döner.

### Git Mirroring (Depoyu Başka Bir Uzak Depoya Kopyalama)

- git clone --mirror <repo_url> – Depoyu aynen klonlar.
- git push --mirror <yeni_repo_url> – Depoyu başka bir uzak depoya aynen kopyalar.

### Branch Yönetimi

- git branch -vv – Tüm dalların detaylarını ve takip ettiği uzak dalı gösterir.
- git branch --contains <commit_id> – Belirtilen commit’i içeren dalları listeler.
- git branch --merged master – master dalına birleştirilmiş dalları gösterir.
- git branch --no-merged master – master dalına henüz birleştirilmemiş dalları gösterir.
- git checkout - – Önceki dalına geri döner.
- git checkout --orphan <yeni_branch_adı> – Yeni bir dal oluşturur ancak önceki commit’leri içermez.

### Merge ve Rebase İşlemleri

- git merge --squash <branch_adı> – Birleştirme işlemi sırasında tüm commit’leri tek bir commit’e sıkıştırır.
- git merge --no-commit – Birleştirme işlemini yapar ancak commit oluşturmaz.
- git merge --no-ff <branch_adı> – Fast-forward olmadan birleştirme yapar.
- git rebase -i HEAD~5 – Son 5 commit’i etkileşimli olarak düzenler.
- git rebase --onto master feature_branch – feature_branch dalını master üzerine taşır.
- git rebase --skip – Rebase sırasında hatalı commit’i atlar.
- git rebase --edit-todo – Rebase sırasında commit listesini düzenler.

### Stash Kullanımı

- git stash push -m "Geçici değişiklikler" – Saklanan değişikliklere açıklama ekler.
- git stash apply stash@{2} – Belirtilen stash’i geri yükler.
- git stash pop stash@{0} – En son saklanan değişiklikleri geri yükler ve stash listesinden siler.
- git stash show -p stash@{1} – Belirtilen stash’in detaylarını gösterir.
- git stash branch yeni_branch – Saklanan değişikliklerle yeni bir dal oluşturur.

### Uzak Depo Yönetimi

- git remote set-url origin <yeni_url> – Uzak depo URL’sini değiştirir.
- git remote prune origin – Uzak depoda artık var olmayan dalları temizler.
- git push origin HEAD – Mevcut dalı uzak depoya gönderir.
- git push --mirror <yeni_repo_url> – Mevcut depoyu aynen başka bir uzak depoya kopyalar.
- git fetch --prune – Uzak depodaki silinmiş dalları yerel depodan kaldırır.

### Hata Ayıklama ve Analiz

- git fsck --full – Depodaki tüm nesneleri kontrol eder ve hataları gösterir.
- git reflog expire --expire=now --all – Tüm reflog kayıtlarını temizler.
- git gc --aggressive – Depoyu optimize eder ve gereksiz verileri temizler.
- git blame -C -M <dosya_adı> – Dosyadaki her satırın hangi commit tarafından değiştirildiğini detaylı gösterir.
- git grep -n "hata" – Depoda belirli bir kelimeyi içeren satırları ve satır numaralarını gösterir.

### Performans ve Optimizasyon

- git repack -a -d – Depoyu yeniden paketleyerek boyutunu küçültür.
- git prune --expire=now – Kullanılmayan nesneleri hemen temizler.
- git gc --auto – Depoyu otomatik olarak temizler ve optimize eder.
- git config --global core.compression 9 – Git’in veri sıkıştırma seviyesini artırır.






































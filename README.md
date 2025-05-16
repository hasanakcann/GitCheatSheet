## 🧠 Git Cheat Sheet

![image](https://github.com/user-attachments/assets/1821b39f-70be-4943-b193-ff8ac46d5b1f)

## 🔍 Git Nedir?

Git, dağıtık bir versiyon kontrol sistemidir (VCS). Yazılımcıların projelerdeki dosya değişikliklerini takip etmelerine, geri almalarına, dallandırmalarına(branch) ve farklı sürümleri yönetmelerine olanak tanır.

![image](https://github.com/user-attachments/assets/86aa12b7-a1ff-489d-9ca6-0f65e3c2b5d8)

## ☁️ GitHub Nedir?

GitHub, Git tabanlı projeleri barındırmak, paylaşmak ve üzerinde işbirliği yapmak için kullanılan bulut tabanlı bir platformdur.

![image](https://github.com/user-attachments/assets/8538d93f-17b9-4952-9380-f7499f0aca40)

## 🛠️ Sık Kullanılan Git Komutları

<details>
  
<summary>🖥️ Git Bash - Commit Example</summary>

Proje dizinine gidilir. **cd source/repos/project**

Sırasıyla komutlar çalıştırılır.

**1.** git pull origin develop

**2.** git status

**3.** git add .

**4.** git commit -m "fixed"

**5.** git push origin develop

</details>

<details>
    
<summary>🔰 Temel Git Komutları</summary>

- **git init** ➡️ Yeni bir Git reposu oluşturur.
- **git clone <repo_url>** ➡️ Mevcut bir Git reposunu kopyalar.
- **git status** ➡️ Çalışma dizininin durumunu gösterir.
- **git add <dosya_adı>** ➡️ Belirtilen dosyayı stage'e (staging area) ekler.
- **git add .** ➡️ Tüm değişiklikleri stage'e ekler.
- **git commit -m "Açıklama"** ➡️ Stage'e alınan değişiklikleri repoya kaydeder.
- **git commit --amend -m "Yeni açıklama"** ➡️ Son commit mesajını değiştirir.
- **git push origin <branch_adı>** ➡️ Local değişiklikleri remote repoya gönderir.
- **git pull origin <branch_adı>** ➡️ Remote repodaki değişiklikleri local repoya çeker.
- **git fetch** ➡️ Remote repodaki değişiklikleri alır ancak merge yapmaz.

</details>

<details>
  
<summary>🌿 Branch Yönetimi</summary>

- **git branch** ➡️ Mevcut branchleri listeler.
- **git branch <yeni_branch_adı>** ➡️ Yeni bir branch oluşturur.
- **git branch -d <branch_adı>** ➡️ Belirtilen branch siler.
- **git branch -D <branch_adı>** ➡️ Zorla branch'i siler.
- **git checkout <branch_adı>** ➡️ Belirtilen branch'e geçiş yapar.
- **git checkout -b <yeni_branch_adı>** ➡️ Yeni bir branch oluşturur ve ona geçiş yapar.
- **git cherry-pick <commit_hash>** ➡️ Bir branch'teki belirli bir değişikliği, başka bir branch'e aktarmak için kullanılır. commit_hash: Cherry-pick yapmak istediğiniz commit'in hash'idir (örneğin, xyz1234 gibi).
- **git merge <branch_adı>** ➡️ Belirtilen branch'i mevcut branch'e birleştirir.
- **git rebase <branch_adı>** ➡️ Mevcut branch'i başka bir branch'in üzerine yeniden düzenler.
- **git stash** ➡️ Geçici olarak değişiklikleri saklar.
- **git stash pop** ➡️ Saklanan değişiklikleri geri yükler.
- **git stash list** ➡️ Saklanan değişiklikleri listeler.
- **git stash drop** ➡️ Belirtilen saklanan değişikliği siler.

</details>

<details>
  
<summary>🧾 Geçmiş ve Değişiklik Takibi</summary>

- **git log** ➡️ Commit geçmişini görüntüler.
- **git log --oneline** ➡️ Commit geçmişini kısa formatta gösterir.
- **git log --graph --decorate --oneline** ➡️ Commit geçmişini branch yapısıyla gösterir.
- **git diff** ➡️ Çalışma dizini ile en son commit arasındaki farkları gösterir.
- **git diff <branch1> <branch2>** ➡️ İki branch arasındaki farkları gösterir.
- **git reset --hard <commit_id>** ➡️ Belirtilen commit’e geri döner ve tüm değişiklikleri siler.
- **git reset --soft <commit_id>** ➡️ Belirtilen commit’e geri döner ancak değişiklikleri korur.
- **git revert <commit_id>** ➡️ Belirtilen commit’i geri alır ancak yeni bir commit olarak ekler.

</details>

<details>
  
<summary>🌐 Uzak Repo Yönetimi</summary>

- **git remote -v** ➡️ Remote repoları listeler.
- **git remote add <name> <repo_url>** ➡️ Yeni bir remote repo ekler.
- **git remote remove <name>** ➡️ Belirtilen remote repoyu kaldırır.
- **git push --force** ➡️ Zorla değişiklikleri remote repoya gönderir.
- **git push origin --delete <branch_adı>** ➡️ Remote repodaki bir branch'i siler.
- **git pull --rebase** ➡️ Remote repodaki değişiklikleri alır ve mevcut commit’leri yeniden düzenler.

</details>

<details>
  
<summary>🔖 Etiketleme ve Sürümleme</summary>

- **git tag <etiket_adı>** ➡️ Belirtilen commit’e bir etiket ekler.
- **git tag -a <etiket_adı> -m "Açıklama"** ➡️ Açıklamalı bir etiket ekler.
- **git tag** ➡️ Mevcut etiketleri listeler.
- **git push origin <etiket_adı>** ➡️ Etiketi remote repoya gönderir.
- **git push origin --tags** ➡️ Tüm etiketleri remote repoya gönderir.
- **git tag -d <etiket_adı>** ➡️ Belirtilen etiketi siler.
- **git push origin :refs/tags/<etiket_adı>** ➡️ Remote repodaki etiketi siler.

</details>

<details>
  
<summary>⚡ Alias (Kısayollar) Kullanımı</summary>

- **git config --global alias.st status** ➡️ git st komutunu git status olarak çalıştırır.
- **git config --global alias.co checkout** ➡️ git co komutunu git checkout olarak çalıştırır.
- **git config --global alias.br branch** ➡️ git br komutunu git branch olarak çalıştırır.

</details>

<details>
  
<summary>🧩 Git Hooks (Otomasyon)</summary>

- **pre-commit** ➡️ Commit işleminden önce çalıştırılır.
- **commit-msg** ➡️ Commit mesajı yazıldıktan sonra çalıştırılır.
- **pre-push** ➡️ Push işleminden önce çalıştırılır.

</details>

<details>
  
<summary>📦 Submodules (Alt Depolar)</summary>

- **git submodule add <repo_url>** ➡️ Mevcut projeye bir alt modül ekler.
- **git submodule update --init --recursive** ➡️ Alt modülleri günceller ve başlatır.

</details>

<details>
  
<summary>🧱 Worktrees (Çoklu Çalışma Dizinleri)</summary>

- **git worktree add ../yeni_dizin <branch_adı>** ➡️ Yeni bir çalışma dizini oluşturur.
- **git worktree list** ➡️ Mevcut çalışma dizinlerini listeler.

</details>

<details>
  
<summary>🧊 LFS (Large File Storage)</summary>

- **git lfs install** ➡️ Git LFS’i yükler.
- **git lfs track "*.psd"** ➡️ Belirtilen dosya türünü LFS ile takip eder.

</details>

<details>
  
<summary>🐞 Bisect (Hatalı Commit’i Bulma)</summary>

- **git bisect start** ➡️ Bisect işlemini başlatır.
- **git bisect bad** ➡️ Hatalı commit’i işaretler.
- **git bisect good**➡️ Çalışan commit’i işaretler.

</details>

<details>
  
<summary>🔁 Reflog (Commit Geçmişi)</summary>

- **git reflog** ➡️ Tüm Git işlemlerinin geçmişini gösterir.
- **git reset --hard HEAD@{3}** ➡️ 3 işlem önceki duruma geri döner.

</details>

<details>
  
<summary>🪞 Mirroring  (Depoyu Başka Bir Uzak Depoya Kopyalama)</summary>

- **git clone --mirror <repo_url>** ➡️ Repoyu aynen klonlar.
- **git push --mirror <yeni_repo_url>** ➡️ Repoyu başka bir remote repoya aynen kopyalar.

</details>

<details>
  
<summary>🌿 İleri Düzey Branch Yönetimi</summary>

- **git branch -vv** ➡️ Tüm branchlerin detaylarını ve takip ettiği remote branch'i gösterir.
- **git branch --contains <commit_id>** ➡️ Belirtilen commit’i içeren branch'leri listeler.
- **git branch --merged master** ➡️ master branch'e merge edilmiş branch'leri gösterir.
- **git branch --no-merged master** ➡️ master branch'e henüz merge edilmemiş branchleri gösterir.
- **git checkout -** ➡️ Önceki branch'e geri döner.
- **git checkout --orphan <yeni_branch_adı>** ➡️ Yeni bir branch oluşturur ancak önceki commit’leri içermez.

</details>

<details>
  
<summary>🔀 Merge ve Rebase İşlemleri</summary>

- **git merge --squash <branch_adı>** ➡️ Merge işlemi sırasında tüm commit’leri tek bir commit’e sıkıştırır.
- **git merge --no-commit** ➡️ Merge işlemini yapar ancak commit oluşturmaz.
- **git merge --no-ff <branch_adı>** ➡️ Fast-forward olmadan merge yapar.
- **git rebase -i HEAD~5** ➡️ Son 5 commit’i etkileşimli olarak düzenler.
- **git rebase --onto master feature_branch** ➡️ feature_branch branch'ini master üzerine taşır.
- **git rebase --skip** ➡️ Rebase sırasında hatalı commit’i atlar.
- **git rebase --edit-todo** ➡️ Rebase sırasında commit listesini düzenler.

</details>

<details>
  
<summary>📥 Stash Kullanımı</summary>

- **git stash push -m "Geçici değişiklikler"** ➡️ Saklanan değişikliklere açıklama ekler.
- **git stash apply stash@{2}** ➡️ Belirtilen stash’i geri yükler.
- **git stash pop stash@{0}** ➡️ En son saklanan değişiklikleri geri yükler ve stash listesinden siler.
- **git stash show -p stash@{1}** ➡️ Belirtilen stash’in detaylarını gösterir.
- **git stash branch yeni_branch** ➡️ Saklanan değişikliklerle yeni bir branch oluşturur.

</details>

<details>
  
<summary>🌐 İleri Düzey Uzak Repo Yönetimi</summary>

- **git remote set-url origin <yeni_url>** ➡️ Remote repo URL’sini değiştirir.
- **git remote prune origin** ➡️ Remote repoda artık var olmayan branch'leri temizler.
- **git push origin HEAD** ➡️ Mevcut branch'i remote repoya gönderir.
- **git push --mirror <yeni_repo_url>** ➡️ Mevcut repoyu aynen başka bir remote repoya kopyalar.
- **git fetch --prune** ➡️ Remote repodaki silinmiş branchleri local repodan kaldırır.

</details>

<details>
  
<summary>🔍 Hata Ayıklama ve Analiz</summary>

- **git fsck --full** ➡️ Repodaki tüm nesneleri kontrol eder ve hataları gösterir.
- **git reflog expire --expire=now --all** ➡️ Tüm reflog kayıtlarını temizler.
- **git gc --aggressive** ➡️ Repoyu optimize eder ve gereksiz verileri temizler.
- **git blame -C -M <dosya_adı>** ➡️ Dosyadaki her satırın hangi commit tarafından değiştirildiğini detaylı gösterir.
- **git grep -n "hata"** ➡️ Repoda belirli bir kelimeyi içeren satırları ve satır numaralarını gösterir.

</details>

<details>
  
<summary>🚀 Performans ve Optimizasyon</summary>

- **git repack -a -d** ➡️ Repoyu yeniden paketleyerek boyutunu küçültür.
- **git prune --expire=now** ➡️ Kullanılmayan nesneleri hemen temizler.
- **git gc --auto** ➡️ Repoyu otomatik olarak temizler ve optimize eder.
- **git config --global core.compression 9** ➡️ Git’in veri sıkıştırma seviyesini artırır.

</details>

</details>

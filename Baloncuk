Adımlar:
1)Baloncuk adında bir repo oluştur. 
Eğer Repon private ise: profile-> settings-> Public Profile-> Include private contributions on my profile
2)Reponun içine: .github/workflows/main.yml dosyası (buradaki "/" ların anlamı yeni klasör oluşturmak. Yani son durumda Baloncuk reponun içinde .github diye bir kalsör olacak. Onun içinde workflows adında bir klasör olacak onun içinde main.yml dosyası olacak.)  
3)Alttaki kodlardan birini yapıştır. (Kodlar çalışıyor. Dikkatli bak =) )
Her Gün Otomatik Etkinlik:
# .github/workflows/main.yml

on:
  schedule:
  - cron: '0 12 * * *' # every day at noon

jobs:
  single-commit:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
    - uses: bcanseco/github-contribution-graph-action@v2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GIT_EMAIL: you@youremail.com # replace me

Bal 10 (Tüm Yıl Tek Kod):
# .github/workflows/main.yml

on: push

jobs:
  backfill-commits:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
    - uses: bcanseco/github-contribution-graph-action@v2
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        GIT_EMAIL: example@gmail.com
        MAX_DAYS: 365
        MIN_COMMITS_PER_DAY: 1
        MAX_COMMITS_PER_DAY: 5

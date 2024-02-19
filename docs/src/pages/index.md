# Vuepress + Cloudflare Pages 使い方

絶対また忘れれるからめも

## Vuepress の初期化

1. Github でレポジトリを作成してクローンする

2. workdirで init

```bash
yarn create vuepress-site
```

3. master以外のプッシュされたら反映させるブランチを作っておく

## Cloudflare Pages の設定

1. Cloudflare Pages でレポジトリを選択して Deploy Branch をページ用ブランチにしておく

2. 以下の設定にしておく
    
Build Command:   
`npx vuepress build src`  
Build Output Directory:   
`src/.vuepress/dist`  
Root Directory:  
`docs`  
Environment Variables:  
`NODE_OPTIONS` = `--openssl-legacy-provider`  

3. index.md を適当に書いてページブランチにPR

4. 結果待ち
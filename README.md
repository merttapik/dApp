
# Moralis NextJS Auth Demo App

Documentation available at https://docs.moralis.io/docs/nextjs-web3-auth

## Kurulum

node modullerinin oluşması için aşağıdaki komutlardan birini kullanın

```javascript
npm install
yarn install
```
# .env.local dosyası ve moralis ile mongodb bağlantısı

öncelikle en üst katmanda .enc.local dosyası oluşturun bu dosyanın içinde bulunması gerekenler

```env
MORALIS_API_KEY=
APP_DOMAIN=dapp
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=
MONGODB_URI=
```
1.moralis apinizi moralis sayfasına üye olup alabilirsiniz
2.nextauthsecretı # Linux: `openssl rand -hex 32`yazarak yada  https://generate-secret.now.sh/32 adresine gidip oluşan sayıyı yazarak tamamlayabilirsiniz.
3.mongodburı yı almak için 3 adım var
3.1 mongodb ye giriş yapın Data Access kısmında yeni kullanıcı oluşturun, isim ve şifreyi unutmayın, build in roleden read and write any database seçin ve kullanıcı ekleyin.
3.2 Network Accessten add ıp address'a tıklayıp Access List Entry: 0.0.0.0/0 olarak girin
3.3 Database kısmında Cluster0 içindeki connecte tıklayın ardından connect your application seçin çıkan url li kopyalayın ve MONGO_URI ye yapıştırın.
ardından oluşturulan userının usernamini ve sifresini girin "/" ile "?" arasında oluşturulacak olan database isminizi girin.
# Uygulamayı localde çalıştırma
öncelikle build alın
```javascript
npm run build
yarn build
```
localde çalıştırmak için  

```javascript
npm run dev
yarn dev
```
localhost:3000 de uygulamanız ayağa kalkacaktır.

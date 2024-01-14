# Notification Front (Listener de Firebase e Pusher)

Essa aplicação é responsável por **escutar** tanto envio de **notifications-pusher** quanto **notifications-firebase**

## Instalação Firebase

### Configurações Firebase

1. Copie e cole as configurações (já criadas) na conta do **console.firebase** para o arquivo **firebase-messaging-sw.js** na pasta public
```js
firebase.initializeApp({
    apiKey: "api-key",
    authDomain: "auth-domian",
    projectId: "project-id",
    storageBucket: "storage-bucket",
    messagingSenderId: "message-sender-id",
    appId: "app-id",
    measurementId: "measurement-id"
});
```

2. Copie e cole as configurações (já criadas) na conta do **console.firebase** para o arquivo **app-firebase.blade.php**
```js
firebase.initializeApp({
    apiKey: "api-key",
    authDomain: "auth-domian",
    projectId: "project-id",
    storageBucket: "storage-bucket",
    messagingSenderId: "message-sender-id",
    appId: "app-id",
    measurementId: "measurement-id"
});
```

### Configurações App

1. Faça uma cópia do arquivo **.env.example** como **.env**
```shell
cp .env.example .env
```

2. Crie um arquivo chamado **database.sqlite** na pasta **database**
```shell
sudo touch database/database.sqlite
```

4. Rode o **composer install**
```shell
composer install
```

5. Faça a migração das tabelas
```shell
php artisan migrate
```

6. Rode os comandos **npm**
```shell
npm install && npm run dev
```

7. Rode a aplicação na porta **8001**
```shell
php artisan serve --port=8001
```

8. Registre um usuário na rota **http://localhost:8001/register** e logue com ele

Obs.: Esse usuário deve também existir no **notifications-firebase**

9. Abra a rota **http://127.0.0.1:8001/app-firebase** e clique no botão **Allow notification**


# rn_firebase_member
rn crud firebase with member (register and sign in sign out)

    step01 新增一firebase應用   
    step02 firebase設定 database ->rules
```
{
    "rules": {
        "users": {
            "$uid": {
                ".read": "$uid === auth.uid",
                ".write": "$uid === auth.uid"
            }
        }
     }
}
```
    step03 修改 根目錄下 src 下 firebase.json 的 KEY值 (改成自己的firebase api key 密鑰)
```
<script src="https://www.gstatic.com/firebasejs/4.10.0/firebase.js"></script>
<script>
  // Initialize Firebase
  var config = {
    apiKey: "",
    authDomain: "",
    databaseURL: "",
    projectId: "",
    storageBucket: "",
    messagingSenderId: ""
  };
  firebase.initializeApp(config);
</script>
```
    step04 設定firebase的Authentication 設定為 電子信箱 登入 enable
    step05 根目錄下npm install
```    
    step06
    打開項目node_modules/react-native/local-cli/server/server.js
　　找到 process.on('uncaughtException', error =>
　　{ 這個方法，把最後一句 process.exit(11); 註釋掉。
```
    step07 run android or xcode 模擬器
    step08 根目錄  react-native run-android(run-ios) 

```
DEMO
```
![image](https://github.com/a68727739/rn_firebase_member/blob/master/demo01.gif)

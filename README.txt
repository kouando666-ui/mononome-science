第13回 物の燃え方：家族用4択学習アプリ（試作版）

1. ローカルで試す：index.html をブラウザで開く（ブラウザによってモジュールの制限があるため、公開URLでの利用を推奨）。Firebase未設定でも端末内に学習記録を保存。
2. GitHubで新規リポジトリを作成。ZIPを展開した中身をアップロード（ZIPそのものではなくファイルをアップロード）。Settings > Pages > Deploy from a branch > main / root を選択。数分後にURLが発行されます。
3. Firebase Consoleでプロジェクト作成 > Authentication > Sign-in method > Email/Password を有効化。Firestore Database を作成し、firestore.rules の内容をFirestoreのルールに設定。
4. Firebaseのプロジェクト設定でWebアプリを登録し、表示された firebaseConfig を firebase-config.js に貼り付けてGitHubへ反映。
5. Firebase Authentication > Settings > Authorized domains に GitHub Pagesのドメイン（ユーザー名.github.io）を必要に応じて追加。
6. アプリの「同期設定」で家族用メールアドレス・パスワードを初回登録。iPhoneとiPadで同じ認証情報でログイン。

注意：
・教材画像は家庭内利用向けに抜粋したものです。公開GitHub Pagesに画像を置くと第三者が閲覧できるため、公開リポジトリへの教材画像アップロードは避けてください。現状の試作版は画像を同梱しており、公開前に画像を削除するか、認証付きの非公開Firebase Storageへ移す必要があります。
・Firebaseの設定情報自体は公開用の識別子ですが、アクセス制御はFirestore Rulesと認証で必ず行ってください。
・同期は最後の更新時刻による簡易方式です。同時に2端末で解答すると後から保存した記録が優先される可能性があります。1台ずつ使ってください。
・問題文は教材の論点をもとに作成したオリジナル4択で、原文の完全転記ではありません。実験図は一部関連図を表示しています。
・初回のChatGPTでの第1問正解は設定画面から登録できます。

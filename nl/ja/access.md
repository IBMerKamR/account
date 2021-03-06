---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: user access, IBM Cloud account access, account owner

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# カタログへのユーザーのアクセス権限の管理
{: #find-access}

{{site.data.keyword.Bluemix}} アカウント所有者は、{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) ポリシーを使用して、ユーザーにカタログへのアクセス権限を割り当てることができます。 アカウント・カタログに追加されたプライベート・サービスやアカウント内に作成されたパブリック・サービスの可視性を制御できます。 デフォルトでは、アカウント所有者のみがこれらのタスクを実行できます。

## アクセス権限の委任
{: #get-access}

アカウントのアクセス権限を委任することによって、ユーザーが何を見ることができるのかを制御でき、また、それらのユーザーがどの程度の権限を持つのかを制御できます。 例えば、ある情報は特定のユーザーが読み取りと分析のみを行うのが適切だが、その情報を編集する権限は別のユーザーに与えられるといったことが考えられます。 アカウントのアクセス権限をアカウント内の別のユーザーに委任するには、以下の手順を実行します。

1. **「管理」** > **「アクセス (IAM)」**をクリックします。
2. ランディング・ページで**「ユーザーで始まるアクセス権限 (Access starts with the user)」**をクリックします。
3. ご使用のアカウントのユーザーを選択します。
4. **「アクセス・ポリシー」**をクリックします。
5. **「アクセス権限の割り当て (Assign access)」**をクリックします。 次に、**「アカウント管理サービスの割り当て」**をクリックします。
6. 「サービス」リストから**「グローバル・リソース・カタログ」**を選択し、「役割の選択」リストから**「管理者」**役割を選択します。

他の権限を付与するには、「ビューアー」役割および「エディター」役割を使用します。 アカウントのカタログで作業するコンテキスト内で、各 IAM 役割がユーザーに許可するアクションについての詳細は、以下の表を確認してください。

| プラットフォーム管理の役割 | アクション                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| ビューアー                   | プライベート・サービスを表示できるが、変更はできない                                                            |
| エディター                   | オブジェクト・メタデータを変更できるが、プライベート・サービスの可視性を変更できない                                |
| 管理者            | オブジェクト・メタデータを変更したりプライベート・サービスの可視性を変更したりでき、パブリック・サービスの可視性を制限することもできる  |
{: caption="表 1. プラットフォーム管理の役割とカタログに対するアクションの例" caption-side="top"}

ユーザーへのアクセス権限の割り当てについて詳しくは、[アカウント管理サービスへのアクセス権限の割り当て](/docs/iam?topic=iam-account-services)を参照してください。

## アクセス権限の確認
{: #confirm-access}

あるユーザーが他の人のアカウントに追加された場合、アカウント管理者は適当なレベルのアクセス権限をそのユーザーに委任して、アカウントに追加されたプライベート・リソースをそのユーザーが表示できるようにすることができます。 アカウント所有者は、アカウント・カタログ内のパブリック・リソースを表示できるようにするために委任することもできます。 デフォルトではこのアクセス権限はありません。 これらのアカウント・リソース管理タスクを実行するためのアクセス権限を持つことができるように IAM 役割をアカウント所有者に付与してもらう必要があります。

{{site.data.keyword.Bluemix_notm}} コンソールまたはコマンド・ライン・インターフェース (CLI) を使用して、アカウント内のプライベート・リソースを特定のユーザーが表示するのを許可するためのアクセス権限が自分にあるかどうかを判断できます。

コンソールを使用するには、以下の手順を実行します。

  1. **「管理」 > 「アクセス (IAM)」**に移動します。
  2. 「ユーザー」のリストから自分の名前をクリックします。
  3. **「アクセス・ポリシー」**タブをクリックします。このタブでは、割り当てられたアクセス・ポリシーを表示できます。 カタログ内のプライベート・リソースを表示するためにアカウントを組み込むリストを更新するには、アカウント内のカタログ・リソースの Cloud IAM 管理者役割を持っていることが必要です。


[CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam) を使用するには、`ibmcloud iam user-policies <your-user-name>` コマンドを実行します。 アカウント管理者でない場合、このコマンドはエラーを返します。

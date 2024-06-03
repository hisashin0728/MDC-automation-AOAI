# MDC-automation-AOAI
>Microsoft Defender for Cloud automation - notification translated by AOAI.

このレポジトリはMicrosoft Defender for Cloud のオートメーション機能を用いて、Azure OpenAI を経由して翻訳・要約して通知するパッケージを掲載しています。

# 構成イメージ
>システム構成イメージ

Microsoft Defender for Cloud の Automation 機能を用いて、アラート/推奨事項の検出時に Azure OpenAI にプロンプトを投げて、回答を Office365 に通知を行います。
![image](https://github.com/hisashin0728/MDC-automation-AOAI/assets/55295601/39af8d43-1d47-40b7-9d65-9dba7462b939)

# デプロイ
> Deploy to Azure

- **推奨事項 (Recommendations)** 通知パッケージ
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhisashin0728%2FMDC-automation-AOAI%2Fmain%2FMDC-automation-recommendation-AOAI.json)
- **セキュリティアラート (CWPP Alert)** 通知パッケージ
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhisashin0728%2FMDC-automation-AOAI%2Fmain%2FMDC-automation-alert-AOAI.json)

# 構成方法
- マネージド ID はデプロイ時に有効化されますが、ロールに「Azure OpenAI ユーザー」の権限を付与して下さい
- RESTAPI で Azure OpenAI に問い合わせする RESTAPI エンドポイント、モデル先をお客様指定のものに変更下さい

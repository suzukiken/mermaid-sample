## これは何

[Githubでコードで図を書くことができる](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)ので、それを使ったサンプルコードです。

自分の練習にも使います。

## 便利なツール

[Live Editor](https://mermaid-js.github.io/mermaid-live-editor/)

## Flow

```mermaid
flowchart TD
    BO[system A] -->|variations as message attribute *1| SNS(SNS):::hyperlink
    SNS --> SQS{SQS}
    SQS --> |request A| LambdaA[Lambda A]
    SQS --> |request B| LambdaB[Lambda B]
    SQS --> |request C| LambdaC[Lambda C]
    LambdaA --> |update A| Shop[system B]
    LambdaB --> |update B| Shop[system B]
    LambdaC --> |update C| Shop[system B]
```

## Flow

```mermaid
flowchart TD
    classDef hyperlink fill:#aaa, color:#00f;
    systemA[System A] -->|イベント *1| EVBG(EventBridge):::hyperlink
    EVBG --> EventRule{EventRule}:::hyperlink
    EventRule --> |event A| SNSA:::hyperlink
    EventRule --> |event B| SNSB:::hyperlink
    click EVBG href "https://github.com/"
    click EventRule href "https://github.com/"
    click SNSA href "https://github.com/"
    click SNSB href "https://github.com/"
```

## Flow

```mermaid
flowchart TD
    S3 --> |JSON| StateA(全商品の最新の情報を得る)
    StateA --> StateB(特定の商品について更新があったか)
    DynamoDB --> |商品の過去の情報| StateB
    StateB --> |くりかえし| StateB
    StateB --> |更新があったのでアップデート要求| SQS
```


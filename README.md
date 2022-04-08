## これは何

Githubでコードで図を書くことができるので、それを使ったサンプルコードです。
https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/

自分の練習にも使います。

## 便利なツール

(Live Editor)[https://mermaid-js.github.io/mermaid-live-editor/]

## Flow

```mermaid
graph TD
    A[Christmas] -->|Get money| B(Go shopping):::hyperlink
    B --> C[Let me think]
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
      click B href "https://github.com/"
      classDef hyperlink fill:#aaa, color:#00f;
```

## 

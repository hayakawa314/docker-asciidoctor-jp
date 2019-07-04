# docker-asciidoctor-jp

[liquidz/docker-asciidoctor-jp](https://github.com/liquidz/docker-asciidoctor-jp/)
を再ビルドしただけです。

[Asciidoctor docker container](https://hub.docker.com/r/asciidoctor/docker-asciidoctor/)
の最新を使用したものをDocker Hubに登録して共有することが目的です。

## 使い方

### コンテナを起動
> docker run --rm -it -v $(pwd):/documents hayakawa314/docker-asciidoctor-jp

### PDFの生成
> asciidoctor-pdf -r asciidoctor-pdf-cjk-kai_gen_gothic -a pdf-style=KaiGenGothicJP foo.adoc

### 図形を含むPDFの生成
> asciidoctor-pdf -r asciidoctor-diagram -r asciidoctor-pdf-cjk-kai_gen_gothic -a pdf-style=KaiGenGothicJP foo.adoc

### HTMLの生成
> asciidoctor -a source-highlighter=highlightjs -a stylesheet=/stylesheets/github.css foo.adoc


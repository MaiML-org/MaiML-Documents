# MaiML Documents

MaiML の文書の Markdown 版を日本語と英語で置くリポジトリ。
Markdown editions of MaiML documents, in Japanese and English.

| 文書 / Document | 日本語 | English | 版 / Version |
|---|---|---|---|
| 運用指針 / Operational Guideline | [ja/guideline.md](ja/guideline.md) | [en/guideline.md](en/guideline.md) | 0.8.14 (Draft) |
| 設計原理 / Manifesto | [ja/manifesto.md](ja/manifesto.md) | [en/manifesto.md](en/manifesto.md) | 1.0.0 (Draft) |

公開サイト / Published site: https://maiml-org.github.io/MaiML-Documents/

## 位置付け / Status

- 運用指針は、MaiML の規格本文及び XML スキーマに適合要求を追加しない **参考文書** である。
  The operational guideline is an **informative** document. It does not add conformity
  requirements to the MaiML standard text or XML schema.
- 設計原理（The MaiML Manifesto）は **非規定** の独立文書であり、**承認前の草案** である。
  The manifesto is a **non-normative**, stand-alone document and a **pre-approval draft**.
- 仕様及び要求事項は JIS K 0200 及び MaiML スキーマが規定する。
  The specification and its requirements are defined by JIS K 0200 and the MaiML schema.
- 運用指針の英語版は**独立には未承認の作業訳**である。
  The English edition of the operational guideline is a **working translation that has not
  been independently approved**.

## 生成物であること / These files are generated

`ja/` 及び `en/` の Markdown は Word 原本から生成した派生表現であり、**このリポジトリで直接編集しない**。
各ファイルのフロントマターに原本のファイル名と SHA-256 を記録している。

The Markdown under `ja/` and `en/` is generated from the Word originals and **must not be
edited here**. The front matter of each file records the name and SHA-256 of its source.

内容を変更するときは、Word 原本を先に新版化し、その確定内容から生成ツールで作り直したうえで、
このリポジトリへ差し替える。版番号だけの置換をしないこと。

To change the content, revise the Word original first, regenerate with the build tool from
that fixed content, and then replace the files here. Do not merely substitute version numbers.

| 生成物 / Generated file | 原本 / Source | 生成ツール / Build tool |
|---|---|---|
| `ja/guideline.md`, `en/guideline.md` | `MaiML_運用指針_OperationalGuideline_v0.8.14.docx` | `build_guideline_markdown_v0_8_14.py` |
| `ja/manifesto.md`, `en/manifesto.md` | `MaiML_Manifesto_論文_v1.0.0.docx`, `MaiML_Manifesto_Paper_English_v1.0.0.docx` | `build_manifesto_markdown_v1_0_0.py` |

図版は各言語の `assets/MaiML_OperationalGuideline_v0.8.14/` に置く。両言語のファイルはバイト一致である。
Figures are placed under `assets/MaiML_OperationalGuideline_v0.8.14/` in each language
directory; the files are byte-identical between the two.

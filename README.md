# StudyBirds paper

An IJCAI-format starter manuscript for **StudyBirds**, formerly StudyOS.
The repository uses the official **IJCAI 2027** LaTeX author kit, retrieved on 20 November 2026.

The draft introduces the project, describes its student workflow and intended instructor feedback loop, and outlines an evaluation. It contains no claimed learning gains, participant results, or established novelty. Authors remain anonymous until the author list and target track are confirmed.

## Open in Overleaf

1. Sign in to Overleaf and connect the intended GitHub account.
2. Choose **New Project → Import from GitHub** and select `vu-duy-tung/StudyBirds-paper`.
3. Set **Main document** to `main.tex` and **Compiler** to **pdfLaTeX**.
4. Recompile. Edit the files in `sections/` and add citations to `references.bib`.

GitHub synchronization requires an eligible Overleaf premium subscription, including qualifying institutional access. Push and pull are manual through the project's GitHub integration. If synchronization is unavailable, download this repository as a ZIP and use **New Project → Upload Project**; that creates an independent copy.

See [Overleaf's GitHub synchronization documentation](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github-synchronization).

## Files

| Path | Purpose |
| --- | --- |
| `main.tex` | Main document, title, author block, and package setup |
| `sections/` | Abstract, introduction, related work, system, evaluation plan, limitations, and conclusion |
| `references.bib` | Two verified starting references; expand the literature review |
| `ijcai27.sty`, `named.bst` | Unmodified official style and bibliography files |
| `template/` | Original example LaTeX/BibTeX files and template provenance |
| `figures/` | Place future paper figures here |

## Compile locally

With a standard TeX Live installation:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=build main.tex
```

With Tectonic:

```sh
mkdir -p build
tectonic --keep-logs --keep-intermediates --outdir build main.tex
```

Both commands write `build/main.pdf`. Build outputs are ignored by Git. The engine compatibility branch in `main.tex` preserves the IJCAI template metadata when using Tectonic; the official style files are unchanged.

## Next writing steps

- Agree on the target track, final contribution, author list, and affiliations.
- Verify the system description against the revision selected for evaluation.
- Expand related work and add a system overview figure.
- Specify the study protocol and data handling before collecting participant evidence.
- Replace the planned evaluation with actual methods and results when available.
- Recheck the target track's formatting and anonymity requirements before submission.

The current [IJCAI 2027 main-track call](https://2027.ijcai.org/ijcai-2027-call-for-papers-main-track/) permits seven body pages and up to two additional reference pages, with an optional ethics statement allowed in either part. This short starter does not attempt to fill that budget. It retains review line numbers and an anonymous author block; that does not by itself make every future addition anonymous.

Official source: [IJCAI Author's Kit](https://ijcai.org/authors_kit/). See [template provenance](template/README.md) for the exact download and checksums.

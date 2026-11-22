# Dziennik decyzji – notes.domowo.app

Blog statyczny (Hugo), publikowany przez Cloudflare Pages. Wpisy powstają jako szkice w prywatnym trackerze
funduszy i trafiają tutaj dopiero po ręcznej akceptacji (zasady D-41: tylko %, opóźnienie ≥ 1 miesiąc, bez kwot).

## Struktura

```
hugo.toml                 nazwa, podtytuł, stopka, menu, taksonomia „serie”
content/_index.md         wstęp na stronie głównej
content/finanse/          sekcja Finanse (wpisy: RRRR-MM-slug.md)
content/metodyka.md, content/o-blogu.md
layouts/                  motyw (na bazie prototypu „Czysta”)
assets/css/main.css
```

**Nowa sekcja**: katalog `content/<sekcja>/` z `_index.md`, pozycja w `[menus]` w `hugo.toml`
i dopisanie sekcji do listy na stronie głównej (`layouts/index.html`, `slice "finanse" …`).

**Wpis**: front matter `title`, `date`, `serie` (np. `["Eksperymenty"]`), `lead`, opcjonalnie `dane_na` (data danych).
`draft: true` – wpis nie trafia na stronę.

## Lokalnie

```bash
hugo server -D        # podgląd z wersjami roboczymi: http://localhost:1313
hugo --minify         # budowa do public/
```

## Cloudflare Pages (jednorazowo)

1. Cloudflare → Workers & Pages → Create → Pages → Connect to Git → repozytorium `HACS9/notes`.
2. Framework preset: **Hugo**; Build command: `hugo --minify`; Output directory: `public`.
3. Environment variables: `HUGO_VERSION` = `0.139.4`.
4. Po pierwszym wdrożeniu: Custom domains → `notes.domowo.app` (rekord DNS doda się sam, domena jest w Cloudflare).

Każdy push do `main` publikuje stronę; inne gałęzie dostają adres podglądu.

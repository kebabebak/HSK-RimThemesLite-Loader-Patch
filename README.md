> [!NOTE]
> The patch is outdated. The bug was fixed in 

# HSK RimThemesLite Loader Patch

Patch for RimWorld HSK 1.5: fixes RimThemesLite custom loader progress text.

## Dependencies

- Harmony
- RimThemesLite

Load this mod after both.

## What it fixes

During startup RimThemesLite logs errors such as:

```text
Could not resolve symbol "1" for string "Completing loading : {0} / {1}{2}".
Could not resolve symbol "2" for string "Completing loading : {0} / {1}{2}".
```

The patch formats affected loader strings with `string.Format` instead of the broken `GrammarResolver` path.

Affected keys:

- `RimThemes_LoaderCompletingLoading`
- `RimThemes_LoaderResolvinfDefs`
- `RimThemes_LoaderSaveFillingWorld`

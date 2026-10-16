# Hudba do not – webový prototyp 0.1

## Co je hotové
- Rozhraní optimalizované pro Safari na iPhonu/iPadu.
- Výběr lokálního audio souboru a dekódování přes Web Audio API.
- Základní monofonní detekce výšky tónu v prohlížeči (YIN-like autocorrelation).
- Export pracovního MusicXML, MIDI a tiskového náhledu do PDF přes tiskový dialog Safari.
- Audio se nikam neodesílá; analýza běží v aktuální kartě.

## Důležitá omezení
- Toto je prototyp, nikoli hotový automatický přepis partitury.
- Nejlépe funguje izolovaná, jednohlasá melodie. Polyfonní nahrávky, akordy, bicí, více nástrojů, dozvuk a rytmus mohou být rozpoznány chybně.
- Rytmus a takty jsou zatím aproximované; MusicXML/MIDI je třeba zkontrolovat a upravit ve Finale.
- PDF je tiskový výstup zjednodušeného náhledu, ne profesionálně vysázená partitura.
- Přímé získání audia z YouTube není v této čistě lokální verzi implementováno. Nejprve je potřeba vybrat audio soubor uložený v zařízení.
- První verze MusicXML ukládá detekované noty do jednoho taktu; je určena pro ověření exportního řetězce, nikoli pro finální sazbu.

## Spuštění
Nejjednodušší je otevřít `index.html` v prohlížeči. Některé funkce Safari mohou být při otevření přímo z aplikace Soubory omezené. Pro instalaci jako PWA je nutné aplikaci umístit na HTTPS hosting; samotný statický web lze hostovat bez backendu. Zpracování zvuku zůstává lokální.

## Další doporučený krok
Ověřit na krátké čisté melodii (10–20 s) a následně doplnit:
1. robustnější segmentaci not a odhad rytmu,
2. správné dělení do taktů a délky not v MusicXML,
3. profesionální sazbu PDF,
4. automatické testy importu MusicXML/MIDI ve Finale.

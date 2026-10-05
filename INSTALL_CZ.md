# SiteOne Racing - průvodce instalací

## 1. Příprava účtu a Downloaderu

Přihlaste se na [Trading Paints](https://www.tradingpaints.com/) přes vlastní iRacing účet. Nainstalujte [Trading Paints Downloader pro Windows](https://www.tradingpaints.com/page/Install) a nechte jej při ježdění běžet. Pro tyto laky používejte s účtem Free typ **Sim-Stamped Number**.

## 2. Cesta A: týmová kolekce

V [kolekci SiteOne Racing](https://www.tradingpaints.com/collections/view/356562/SiteOne-Racing) otevřete lak přesného modelu vozu, zvolte Dark nebo Light a klikněte **Race this paint**. Zkontrolujte přiřazení v **My Paints**. Tato cesta nevyžaduje ruční nahrávání souborů.

## 3. Cesta B: stažení souborů z GitHubu

Otevřete [veřejný archiv / cars](https://github.com/Buchtanen/siteone-iracing-liveries/tree/main/cars), model a podsložku **dark** nebo **light**:

| Model | Složka |
|---|---|
| BMW M4 GT3 EVO | `cars/bmw-m4-gt3/dark` nebo `light` |
| Ford Mustang GT3 | `cars/ford-mustang-gt3/dark` nebo `light` |
| Porsche 911 GT3 R (992) | `cars/porsche-992-gt3-r/dark` nebo `light` |
| McLaren 720S GT3 EVO | `cars/mclaren-720s-gt3-evo/dark` nebo `light` |

Otevřete **paint.tga** a stáhněte jej přes **Download raw file** (ikona stažení). Ze stejné složky stejně stáhněte **spec.mip**. Uložte dvojici do vlastní složky pro auto a barvu, například BMW-Dark. Oba soubory musí patřit ke stejnému autu a stejné variantě. Nepoužívejte uložení webové stránky jako HTML. Pro upload není potřeba měnit jméno na vaše iRacing ID.

## 4. Nahrání TGA a MIP pod vlastním účtem

1. Otevřete [formulář nahrání](https://www.tradingpaints.com/upload/showroom) v přihlášeném Trading Paints.
2. Přes **Select a paint file** vložte **paint.tga**.
3. Přes **Add spec map or decal layer** otevřete doplňkové soubory. Do části **spec map** vložte **spec.mip**. U McLarenu 570S GT4 Light V78 do decal layer vložte také **decals.tga**; u ostatních stávajících balíčků samostatný decals soubor není.
4. U **Who can race with this paint?** zvolte **Just Me**. Tím se lak uloží do vašich **My Paints**; nevytváříte další veřejnou kopii v Showroomu.
5. V **Vehicle** vyberte přesný vůz. S účtem Free zvolte **Sim-Stamped Number**. Dokončete formulář a uložte jej.
6. V [My Paints](https://www.tradingpaints.com/dashboard) ověřte přiřazený vůz a lak. Nechte Downloader synchronizovat soubory.

| Soubor | Kam patří |
|---|---|
| `paint.tga` | Hlavní paint file: barvy a grafika; u starších variant také loga |
| `decals.tga` | Samostatná loga a polepy pro McLaren 570S GT4 Light V78 |
| `spec.mip` | Spec map: povrch, lesk a metalíza |
| Zdrojové spec TGA | Pracovní podklad; hotový MIP už je v archivu |
| PSD / ZIP | Pracovní soubory pro úpravy, nenahrávat jako lak |
| Studiový PNG render | Katalogové preview, nenahrávat jako texturu |

### McLaren 570S GT4 Light V78 — 5. 10. 2026

Aktuální `paint.tga` pro světlý McLaren 570S GT4 V78 je **Sim-Stamped Number**: původní číselné tabulky jsou prázdné a závodní číslo přidává iRacing. Jedničky v patternu a dekorativní motivy mimo tabulky zůstávají součástí designu. Nahrajte znovu všechny tři aktuální soubory **paint.tga + decals.tga + spec.mip**; samotná aktualizace GitHubu nenahradí dřívější upload na Trading Paints.

Používejte **Sim-Stamped Number**, nikoli Custom Number. V iRacingu ponechte zobrazování herních čísel zapnuté. Pokud jste dříve testovali vlastní čísla, zálohujte mimo složku vozu starý `car_num_VASE-ID.tga` a případný starý `decal_VASE-ID.tga`. Při lokálním testování používejte `car_VASE-ID.tga`; starý soubor `car_num_...` může mít přednost a skrýt číslo hry.

V Paint Shopu porovnáte tovární umístění vypnutím **Show Custom Paint**. Potom vlastní lak znovu zapněte a nechte **Show Stamps** zapnuté. Barva číslic musí kontrastovat s tabulkou: černá pro bílé tabulky 570S/Radical, bílá pro tmavé tabulky GT3.

## 5. Helma a kombinéza

- [TGA týmové helmy](https://raw.githubusercontent.com/Buchtanen/siteone-iracing-liveries/main/gear/helmet/paint.tga) ze složky `gear/helmet`.
- [TGA Crew Suit](https://raw.githubusercontent.com/Buchtanen/siteone-iracing-liveries/main/gear/driver-suit/paint.tga) ze složky `gear/driver-suit`.

Oba soubory mají stejné jméno: uložte je zvlášť nebo jako `helmet.tga` a `suit.tga`. Každý nahrajte samostatně ve stejném formuláři přes **Select a paint file**, vyberte **Just Me** a v **Vehicle** odpovídající typ vybavení (helma nebo kombinéza). **Helma ani kombinéza nepoužívají MIP.** Free používá společnou výbavu pro všechny vozy; různé vybavení podle vozu je funkce Pro.

## 6. Kontrola v iRacingu

Nechte zapnuté **Update my own paints** a **Automatically refresh paints**. Pro náhled mimo session pomáhá **Keep my paints synced from website**. Zkontrolujte auto v Paint Shopu a vybavení přes **Design Your Helmet / Design Your Suit**. Zapněte vlastní lak; starý náhled může obnovit vypnutí a zapnutí jeho přepínače. V session lze obnovit laky pomocí **Ctrl + R**.

Pro spec mapy nastavte Shader Quality alespoň Medium a zapněte Shadow Maps. Jestliže jste dříve ručně testovali materiály, zkontrolujte, zda v lokální složce vozu nezůstalo staré `car_spec_VASE-ID.tga`: iRacing z něj znovu vytváří MIP a může tím přepsat stažený povrch. Zálohujte jej mimo paint složku.

## Ověřené zdroje

- [Formulář, pole pro TGA/MIP a volba Just Me](https://help.tradingpaints.com/showroom/how-do-i-submit-my-work-to-the-showroom/)
- [Spec mapy a MIP](https://help.tradingpaints.com/painting/how-do-i-create-a-spec-map-file-for-use-in-iracing/)
- [Lak ze Showroomu](https://help.tradingpaints.com/showroom/how-can-i-race-with-a-paint-from-the-showroom/)
- [Výbava pro jednotlivé vozy](https://help.tradingpaints.com/trading-paints-pro/how-can-i-use-a-different-helmet-or-suit-for-each-car/)
- [Zobrazení materiálů](https://help.tradingpaints.com/downloader/enabling-custom-spec-maps-in-your-iracing-graphics-options/)

Ověřeno 2. 10. 2026. Studiové rendery v katalogu jsou ilustrační; herní podobu určují TGA a MIP.

---
description: Dans certains cas, une application doit être en mesure d’énumérer les polices disponibles et de sélectionner celle qui convient le mieux à une opération particulière.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Énumération des polices installées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbbf8ba60c9a26b2aa2c6815d08f5d9b342bd4ba6a48c26ce800a37c5a2a371
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718059"
---
# <a name="enumerating-the-installed-fonts"></a>Énumération des polices installées

Dans certains cas, une application doit être en mesure d’énumérer les polices disponibles et de sélectionner celle qui convient le mieux à une opération particulière. Une application peut énumérer les polices disponibles en appelant la fonction [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) ou [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) . Ces fonctions envoient des informations sur les polices disponibles à une fonction de rappel que l’application fournit. La fonction de rappel reçoit des informations dans les structures [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) et [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . (La structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contient des informations sur une police TrueType. Lorsque la fonction de rappel reçoit des informations sur une police non TrueType, les informations sont contenues dans une structure [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) À l’aide de ces informations, une application peut limiter les choix de l’utilisateur aux seules polices disponibles.

La fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) est similaire à la fonction [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , mais elle comprend des fonctionnalités supplémentaires. **EnumFontFamilies** permet à une application de tirer parti des styles disponibles avec les polices TrueType. Les applications nouvelles et mises à niveau doivent utiliser **EnumFontFamilies** au lieu de **EnumFonts**.

Les polices TrueType sont organisées autour d’un nom de police (par exemple, Courier New) et de noms de style (par exemple, italique, gras et gras). La fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) énumère tous les styles associés à un nom de famille spécifié, pas seulement les attributs gras et italique. Par exemple, lorsque le système comprend une police TrueType nommée Courier New Extra-Bold, **EnumFontFamilies** le répertorie avec les autres polices Courier New. Les fonctionnalités de **EnumFontFamilies** sont utiles pour les polices avec des styles nombreux ou inhabituels et pour les polices qui traversent les bordures internationales.

Si une application ne fournit pas de nom de police, les fonctions [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) et [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) fournissent des informations sur une police dans chaque famille disponible. Pour énumérer toutes les polices dans un contexte de périphérique, l’application peut spécifier une **valeur null** pour le nom de la police, compiler une liste des polices disponibles, puis énumérer chaque police dans chaque caractère.

L’exemple suivant utilise la fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) pour récupérer le nombre de familles de polices Raster, vector et TrueType disponibles.


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



Cet exemple utilise deux masques, Raster \_ FONTTYPE et TrueType \_ FONTTYPE, pour déterminer le type de police énuméré. Si le \_ bit FONTTYPE Raster est défini, la police est une police raster. Si le \_ bit TrueType FONTTYPE est défini, la police est une police TrueType. Si aucun bit n’est défini, la police est une police vectorielle. Un troisième masque, \_ FONTTYPE d’appareil, est défini lorsqu’un appareil (par exemple, une imprimante laser) prend en charge le téléchargement des polices TrueType ; il est égal à zéro si l’appareil est une carte d’affichage, une imprimante matricielle ou un autre périphérique raster. Une application peut également utiliser le \_ masque FONTTYPE d’appareil pour distinguer les polices Raster fournies par GDI des polices fournies par l’appareil. Le système peut simuler des attributs gras, italique, souligné et barré pour les polices Raster fournies par GDI, mais pas pour les polices fournies par l’appareil.

Une application peut également vérifier les bits 1 et 2 dans le membre **tmPitchAndFamily** de la structure [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) pour identifier une police TrueType. Si le bit 1 est 0 et que le bit 2 est 1, la police est une police TrueType.

Les polices vectorielles sont classées comme \_ jeux de caractères OEM et non ANSI \_ CharSet. Certaines applications identifient les polices vectorielles à l’aide de ces informations, en vérifiant le membre **tmCharSet** de la structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . Cette catégorisation empêche généralement le mappeur de polices de choisir des polices vectorielles, sauf si elles sont spécifiquement demandées. (La plupart des applications n’utilisent plus les polices vectorielles, car leurs traits sont des lignes uniques et leur dessin prend plus de temps que les polices TrueType, qui offrent un grand nombre des mêmes fonctionnalités de mise à l’échelle et de rotation que les polices vectorielles requises.)

 

 

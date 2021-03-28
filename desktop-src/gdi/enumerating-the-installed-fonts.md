---
description: Dans certains cas, une application doit être en mesure d’énumérer les polices disponibles et de sélectionner celle qui convient le mieux à une opération particulière.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Énumération des polices installées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202041"
---
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="98197-103">Énumération des polices installées</span><span class="sxs-lookup"><span data-stu-id="98197-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="98197-104">Dans certains cas, une application doit être en mesure d’énumérer les polices disponibles et de sélectionner celle qui convient le mieux à une opération particulière.</span><span class="sxs-lookup"><span data-stu-id="98197-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="98197-105">Une application peut énumérer les polices disponibles en appelant la fonction [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) ou [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) .</span><span class="sxs-lookup"><span data-stu-id="98197-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="98197-106">Ces fonctions envoient des informations sur les polices disponibles à une fonction de rappel que l’application fournit.</span><span class="sxs-lookup"><span data-stu-id="98197-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="98197-107">La fonction de rappel reçoit des informations dans les structures [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) et [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="98197-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="98197-108">(La structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contient des informations sur une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="98197-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="98197-109">Lorsque la fonction de rappel reçoit des informations sur une police non TrueType, les informations sont contenues dans une structure [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) À l’aide de ces informations, une application peut limiter les choix de l’utilisateur aux seules polices disponibles.</span><span class="sxs-lookup"><span data-stu-id="98197-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="98197-110">La fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) est similaire à la fonction [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , mais elle comprend des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="98197-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="98197-111">**EnumFontFamilies** permet à une application de tirer parti des styles disponibles avec les polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="98197-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="98197-112">Les applications nouvelles et mises à niveau doivent utiliser **EnumFontFamilies** au lieu de **EnumFonts**.</span><span class="sxs-lookup"><span data-stu-id="98197-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="98197-113">Les polices TrueType sont organisées autour d’un nom de police (par exemple, Courier New) et de noms de style (par exemple, italique, gras et gras).</span><span class="sxs-lookup"><span data-stu-id="98197-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="98197-114">La fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) énumère tous les styles associés à un nom de famille spécifié, pas seulement les attributs gras et italique.</span><span class="sxs-lookup"><span data-stu-id="98197-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="98197-115">Par exemple, lorsque le système comprend une police TrueType nommée Courier New Extra-Bold, **EnumFontFamilies** le répertorie avec les autres polices Courier New.</span><span class="sxs-lookup"><span data-stu-id="98197-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="98197-116">Les fonctionnalités de **EnumFontFamilies** sont utiles pour les polices avec des styles nombreux ou inhabituels et pour les polices qui traversent les bordures internationales.</span><span class="sxs-lookup"><span data-stu-id="98197-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="98197-117">Si une application ne fournit pas de nom de police, les fonctions [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) et [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) fournissent des informations sur une police dans chaque famille disponible.</span><span class="sxs-lookup"><span data-stu-id="98197-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="98197-118">Pour énumérer toutes les polices dans un contexte de périphérique, l’application peut spécifier une **valeur null** pour le nom de la police, compiler une liste des polices disponibles, puis énumérer chaque police dans chaque caractère.</span><span class="sxs-lookup"><span data-stu-id="98197-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="98197-119">L’exemple suivant utilise la fonction [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) pour récupérer le nombre de familles de polices Raster, vector et TrueType disponibles.</span><span class="sxs-lookup"><span data-stu-id="98197-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


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



<span data-ttu-id="98197-120">Cet exemple utilise deux masques, Raster \_ FONTTYPE et TrueType \_ FONTTYPE, pour déterminer le type de police énuméré.</span><span class="sxs-lookup"><span data-stu-id="98197-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="98197-121">Si le \_ bit FONTTYPE Raster est défini, la police est une police raster.</span><span class="sxs-lookup"><span data-stu-id="98197-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="98197-122">Si le \_ bit TrueType FONTTYPE est défini, la police est une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="98197-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="98197-123">Si aucun bit n’est défini, la police est une police vectorielle.</span><span class="sxs-lookup"><span data-stu-id="98197-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="98197-124">Un troisième masque, \_ FONTTYPE d’appareil, est défini lorsqu’un appareil (par exemple, une imprimante laser) prend en charge le téléchargement des polices TrueType ; il est égal à zéro si l’appareil est une carte d’affichage, une imprimante matricielle ou un autre périphérique raster.</span><span class="sxs-lookup"><span data-stu-id="98197-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="98197-125">Une application peut également utiliser le \_ masque FONTTYPE d’appareil pour distinguer les polices Raster fournies par GDI des polices fournies par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98197-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="98197-126">Le système peut simuler des attributs gras, italique, souligné et barré pour les polices Raster fournies par GDI, mais pas pour les polices fournies par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98197-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="98197-127">Une application peut également vérifier les bits 1 et 2 dans le membre **tmPitchAndFamily** de la structure [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) pour identifier une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="98197-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="98197-128">Si le bit 1 est 0 et que le bit 2 est 1, la police est une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="98197-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="98197-129">Les polices vectorielles sont classées comme \_ jeux de caractères OEM et non ANSI \_ CharSet.</span><span class="sxs-lookup"><span data-stu-id="98197-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="98197-130">Certaines applications identifient les polices vectorielles à l’aide de ces informations, en vérifiant le membre **tmCharSet** de la structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="98197-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="98197-131">Cette catégorisation empêche généralement le mappeur de polices de choisir des polices vectorielles, sauf si elles sont spécifiquement demandées.</span><span class="sxs-lookup"><span data-stu-id="98197-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="98197-132">(La plupart des applications n’utilisent plus les polices vectorielles, car leurs traits sont des lignes uniques et leur dessin prend plus de temps que les polices TrueType, qui offrent un grand nombre des mêmes fonctionnalités de mise à l’échelle et de rotation que les polices vectorielles requises.)</span><span class="sxs-lookup"><span data-stu-id="98197-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 

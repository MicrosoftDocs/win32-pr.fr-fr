---
description: 'La classe FontFamily fournit les méthodes suivantes qui récupèrent différentes mesures pour une combinaison famille/style particulière :'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Obtention de métriques de police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033965"
---
# <a name="obtaining-font-metrics"></a><span data-ttu-id="048d4-103">Obtention de métriques de police</span><span class="sxs-lookup"><span data-stu-id="048d4-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="048d4-104">La classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fournit les méthodes suivantes qui récupèrent différentes mesures pour une combinaison famille/style particulière :</span><span class="sxs-lookup"><span data-stu-id="048d4-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="048d4-105">[**FontFamily :: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="048d4-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="048d4-106">[**FontFamily :: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="048d4-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="048d4-107">[**FontFamily :: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="048d4-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="048d4-108">[**FontFamily :: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="048d4-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="048d4-109">Les nombres retournés par ces méthodes sont des unités de conception de police, donc ils sont indépendants de la taille et des unités d’un objet de [**police**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) particulier.</span><span class="sxs-lookup"><span data-stu-id="048d4-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="048d4-110">L’illustration suivante montre les jambages ascendants, descendants et de ligne.</span><span class="sxs-lookup"><span data-stu-id="048d4-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![diagramme de deux caractères sur les lignes adjacentes, montrant la hauteur des cellules, la descente des cellules et l’espacement des lignes](images/fontstext7a.png)

<span data-ttu-id="048d4-112">L’exemple suivant affiche les métriques du style normal de la famille de polices Arial.</span><span class="sxs-lookup"><span data-stu-id="048d4-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="048d4-113">Le code crée également un objet de [**police**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basé sur la famille Arial) avec une taille de 16 pixels et affiche les métriques (en pixels) de cet objet de **police** particulier.</span><span class="sxs-lookup"><span data-stu-id="048d4-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



<span data-ttu-id="048d4-114">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="048d4-114">The following illustration shows the output of the preceding code.</span></span>

![capture d’écran d’une fenêtre avec du texte qui indique la taille de police et la hauteur, ainsi que l’espacement ascendant, descendant et de ligne](images/fontstext8.png)

<span data-ttu-id="048d4-116">Notez les deux premières lignes de la sortie de l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="048d4-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="048d4-117">L’objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retourne une taille de 16, et l’objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) retourne une hauteur em de 2 048.</span><span class="sxs-lookup"><span data-stu-id="048d4-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="048d4-118">Ces deux nombres (16 et 2 048) sont la clé de la conversion entre les unités de conception de police et les unités (en l’occurrence, les pixels) de l’objet **font** .</span><span class="sxs-lookup"><span data-stu-id="048d4-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="048d4-119">Par exemple, vous pouvez convertir la hauteur des unités de conception en pixels comme suit :</span><span class="sxs-lookup"><span data-stu-id="048d4-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![équation qui multiplie 1854 unités de conception par 16 pixels divisée par unités de conception 2048, en équivalent à 14,484375 pixels](images/fontstext9.png)

<span data-ttu-id="048d4-121">Le code précédent positionne le texte verticalement en définissant le membre de données *y* d’un objet [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) .</span><span class="sxs-lookup"><span data-stu-id="048d4-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="048d4-122">La coordonnée y est augmentée `font.GetHeight(0.0f)` de pour chaque nouvelle ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="048d4-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="048d4-123">La méthode [**font :: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) d’un objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retourne l’interligne (en pixels) de cet objet **font** particulier.</span><span class="sxs-lookup"><span data-stu-id="048d4-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="048d4-124">Dans cet exemple, le nombre retourné par **font :: GetHeight** est 18,398438.</span><span class="sxs-lookup"><span data-stu-id="048d4-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="048d4-125">Notez que ce nombre est le même que celui obtenu en convertissant la métrique d’interligne en pixels.</span><span class="sxs-lookup"><span data-stu-id="048d4-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 

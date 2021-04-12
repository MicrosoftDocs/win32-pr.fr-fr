---
description: L’exemple suivant appelle ScriptGetProperties pour déterminer si le script de chacun des éléments successifs requiert la mise en forme du glyphe.
ms.assetid: 75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7
title: Déterminer si un script nécessite la mise en forme de glyphes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eb20fb0335c5779352f15221653dad0c5320c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210056"
---
# <a name="determining-if-a-script-requires-glyph-shaping"></a><span data-ttu-id="6ddbb-103">Déterminer si un script nécessite la mise en forme de glyphes</span><span class="sxs-lookup"><span data-stu-id="6ddbb-103">Determining If a Script Requires Glyph Shaping</span></span>

<span data-ttu-id="6ddbb-104">L’exemple suivant appelle [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) pour déterminer si le script de chacun des [éléments](uniscribe-glossary.md) successifs requiert la mise en forme du glyphe.</span><span class="sxs-lookup"><span data-stu-id="6ddbb-104">The following example calls [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) to find out if the script of each of several successive [items](uniscribe-glossary.md) requires glyph shaping.</span></span>


```C++
const SCRIPT_PROPERTIES **g_ppScriptProperties;
int g_iMaxScript;

WCHAR *pwcInChars = L"Unicode string to itemize";
int cInChars = wcslen(pwcInChars);
const int cMaxItems = 20;
SCRIPT_ITEM si[cMaxItems + 1];
SCRIPT_ITEM *pItems = si;
int cItems;

ScriptGetProperties(&g_ppScriptProperties,
                    &g_iMaxScript);

HRESULT hResult = ScriptItemize(pwcInChars,
                                cInChars,
                                cMaxItems,
                                NULL,
                                NULL,
                                pItems,
                                &cItems);
if (hResult == 0) {
    for (int i=0; i<cItems; i++) {
        if (g_ppScriptProperties[pItems[i].a.eScript]->fComplex) {

            // Item [i] is complex script text
            // requiring glyph shaping.

        } else {

            // The text may be rendered legibly without using Uniscribe. 
            // However, Uniscribe may still be used as a means of accessing 
            // font typographic features. 
        }
    }
} else {
    // Handle the error.
}
```



## <a name="related-topics"></a><span data-ttu-id="6ddbb-105">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ddbb-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ddbb-106">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="6ddbb-106">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




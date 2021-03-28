---
description: Vous pouvez déterminer le nombre de couleurs prises en charge par un appareil et l’utilisation de ces couleurs en extrayant le nombre de couleurs du périphérique et en énumérant les couleurs des plumes solides.
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: Énumération des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972679"
---
# <a name="enumerating-colors"></a>Énumération des couleurs

Vous pouvez déterminer le nombre de couleurs prises en charge par un appareil et l’utilisation de ces couleurs en extrayant le nombre de couleurs du périphérique et en énumérant les couleurs des plumes solides. Pour récupérer le nombre de couleurs, utilisez la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) avec la valeur NUMCOLORS. Pour énumérer des stylets solides, utilisez la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) et une fonction de rappel correspondante qui reçoit des informations sur chaque stylet.


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 




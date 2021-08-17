---
title: Récupérer les attributs des objets, sélectionner de nouveaux objets
description: Une application peut récupérer les attributs d’un stylet, d’un pinceau, d’une palette, d’une police ou d’une image bitmap en appelant les fonctions GetCurrentObject et GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c58d946f61a6a83dcfeb2ddae24d735d3596e5e864cf672bab832d7db3aedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886143"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Récupérer les attributs des objets, sélectionner de nouveaux objets

Une application peut récupérer les attributs d’un stylet, d’un pinceau, d’une palette, d’une police ou d’une image bitmap en appelant les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . La fonction **GetCurrentObject** retourne un handle identifiant l’objet actuellement sélectionné dans le DC ; la fonction **GetObject** retourne une structure qui décrit les attributs de l’objet.

L’exemple suivant montre comment une application peut récupérer les attributs de pinceau actuels et utiliser les données récupérées pour déterminer s’il est nécessaire de sélectionner un nouveau pinceau.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> L’application a enregistré la poignée de pinceau d’origine lors de l’appel de la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) la première fois. Ce descripteur est enregistré afin que le pinceau d’origine puisse être sélectionné à nouveau dans le DC une fois que la dernière opération de peinture est terminée avec le nouveau pinceau. Une fois le pinceau d’origine sélectionné à nouveau dans le DC, le nouveau pinceau est supprimé, ce qui libère de la mémoire dans le tas GDI.

 

 

 




---
description: Tous les périphériques de sortie ne prennent pas en charge l’ensemble des fonctions graphiques.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Récupération des fonctionnalités d’une imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972522"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="b535f-103">Récupération des fonctionnalités d’une imprimante</span><span class="sxs-lookup"><span data-stu-id="b535f-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="b535f-104">Tous les périphériques de sortie ne prennent pas en charge l’ensemble des fonctions graphiques.</span><span class="sxs-lookup"><span data-stu-id="b535f-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="b535f-105">Par exemple, en raison de limitations matérielles, la plupart des traceurs vectoriels ne prennent pas en charge les transferts de bloc de bits.</span><span class="sxs-lookup"><span data-stu-id="b535f-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="b535f-106">Une application peut déterminer si un appareil prend en charge une fonction graphique particulière en appelant la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant l’index approprié et en examinant la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b535f-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="b535f-107">L’exemple suivant montre comment une application teste une imprimante pour déterminer si elle prend en charge les transferts de bloc de bits.</span><span class="sxs-lookup"><span data-stu-id="b535f-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 




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
# <a name="retrieving-the-capabilities-of-a-printer"></a>Récupération des fonctionnalités d’une imprimante

Tous les périphériques de sortie ne prennent pas en charge l’ensemble des fonctions graphiques. Par exemple, en raison de limitations matérielles, la plupart des traceurs vectoriels ne prennent pas en charge les transferts de bloc de bits. Une application peut déterminer si un appareil prend en charge une fonction graphique particulière en appelant la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant l’index approprié et en examinant la valeur de retour.

L’exemple suivant montre comment une application teste une imprimante pour déterminer si elle prend en charge les transferts de bloc de bits.


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



 

 




---
description: L’exemple suivant montre comment une application peut récupérer la couleur actuelle du pinceau DC à l’aide des fonctions SetDCBrushColor et GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Définition et récupération de la valeur de couleur du pinceau de contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0bfc918f5882baa46208d27973e14b9446909e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010632"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a><span data-ttu-id="fac27-103">Définition et récupération de la valeur de couleur du pinceau de contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="fac27-103">Setting and Retrieving the Device Context Brush Color Value</span></span>

<span data-ttu-id="fac27-104">L’exemple suivant montre comment une application peut récupérer la couleur actuelle du pinceau DC à l’aide des fonctions [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) et [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .</span><span class="sxs-lookup"><span data-stu-id="fac27-104">The following example shows how an application can retrieve the current DC brush color by using the [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) and the [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) functions.</span></span>


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 




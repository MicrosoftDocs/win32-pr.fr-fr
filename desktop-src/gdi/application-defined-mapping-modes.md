---
description: Les deux modes de mappage définis par l’application (MM \_ isotropes et mm \_ anisotrope) sont fournis pour les modes de mappage spécifiques à l’application.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modes de mappage Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991292"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="40947-103">Modes de mappage Application-Defined</span><span class="sxs-lookup"><span data-stu-id="40947-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="40947-104">Les deux modes de mappage définis par l’application (MM \_ isotropes et mm \_ anisotrope) sont fournis pour les modes de mappage spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="40947-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="40947-105">Le \_ mode mm isotrope garantit que les unités logiques de l’axe x et de l’axe y sont égales, tandis que le \_ mode anisotrope mm permet aux unités de différer.</span><span class="sxs-lookup"><span data-stu-id="40947-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="40947-106">Une application de CAO ou de dessin peut tirer parti du \_ mode de mappage isotrope de mm, mais elle peut avoir besoin de spécifier des unités logiques qui correspondent aux incréments de l’échelle d’un ingénieur (1/64 pouces).</span><span class="sxs-lookup"><span data-stu-id="40947-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="40947-107">Ces unités seraient difficiles à obtenir avec les modes de mappage prédéfinis (MM \_ HIENGLISH ou mm \_ HIMETRIC); Toutefois, elles peuvent être facilement obtenues en sélectionnant le \_ mode mm isotrope (ou mm \_ anisotrope).</span><span class="sxs-lookup"><span data-stu-id="40947-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="40947-108">L’exemple suivant montre comment définir des unités logiques sur 1/64 pouce :</span><span class="sxs-lookup"><span data-stu-id="40947-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 




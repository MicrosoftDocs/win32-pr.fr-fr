---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510828"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="d5d48-103">IAgentPropertySheet :: GetPosition</span><span class="sxs-lookup"><span data-stu-id="d5d48-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="d5d48-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5d48-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="d5d48-105">Récupère la position de la fenêtre de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d5d48-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="d5d48-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d5d48-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d5d48-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="d5d48-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="d5d48-108">Adresse d’une variable qui reçoit les coordonnées d’écran du bord gauche de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="d5d48-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="d5d48-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="d5d48-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="d5d48-110">Adresse d’une variable qui reçoit les coordonnées d’écran du bord supérieur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="d5d48-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d5d48-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d48-111">See Also</span></span>

[<span data-ttu-id="d5d48-112">**IAgentPropertySheet :: est à obtenir**</span><span class="sxs-lookup"><span data-stu-id="d5d48-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 





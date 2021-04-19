---
title: IAgentPropertySheet
description: IAgentPropertySheet
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510612"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="b715b-103">IAgentPropertySheet :: est à obtenir</span><span class="sxs-lookup"><span data-stu-id="b715b-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="b715b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b715b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="b715b-105">Récupère la taille de la fenêtre de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b715b-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="b715b-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b715b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b715b-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="b715b-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="b715b-108">Adresse d’une variable qui reçoit la largeur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="b715b-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b715b-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="b715b-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="b715b-110">Adresse d’une variable qui reçoit la hauteur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="b715b-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b715b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b715b-111">See Also</span></span>

[<span data-ttu-id="b715b-112">**IAgentPropertySheet :: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="b715b-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 





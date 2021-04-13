---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311599"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="5fcb1-103">IAgentCharacter :: GetPosition</span><span class="sxs-lookup"><span data-stu-id="5fcb1-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="5fcb1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fcb1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="5fcb1-105">Récupère la position du frame d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="5fcb1-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5fcb1-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="5fcb1-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="5fcb1-108">Adresse d’une variable qui reçoit la coordonnée d’écran du bord gauche du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="5fcb1-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="5fcb1-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="5fcb1-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="5fcb1-110">Adresse d’une variable qui reçoit la coordonnée d’écran du bord supérieur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="5fcb1-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="5fcb1-111">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="5fcb1-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fcb1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fcb1-112">See Also</span></span>

<span data-ttu-id="5fcb1-113">[**IAgentCharacter :: SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter ::** de](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="5fcb1-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 





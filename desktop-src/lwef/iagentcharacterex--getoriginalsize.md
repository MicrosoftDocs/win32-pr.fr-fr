---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029026"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="dd852-103">IAgentCharacterEx::GetOriginalSize</span><span class="sxs-lookup"><span data-stu-id="dd852-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="dd852-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd852-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="dd852-105">Récupère la taille d’origine du frame d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="dd852-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="dd852-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="dd852-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dd852-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="dd852-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="dd852-108">Adresse d’une variable qui reçoit la largeur d’origine du cadre d’animation de caractères en pixels.</span><span class="sxs-lookup"><span data-stu-id="dd852-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dd852-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="dd852-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="dd852-110">Adresse d’une variable qui reçoit la hauteur d’origine du cadre d’animation de caractères en pixels.</span><span class="sxs-lookup"><span data-stu-id="dd852-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="dd852-111">Cet appel retourne la taille d’origine de la trame de caractères telle qu’elle est créée dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="dd852-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd852-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd852-112">See Also</span></span>

[<span data-ttu-id="dd852-113">**IAgentCharacter :: est à obtenir**</span><span class="sxs-lookup"><span data-stu-id="dd852-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 





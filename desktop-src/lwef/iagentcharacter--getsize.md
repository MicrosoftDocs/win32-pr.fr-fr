---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311596"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="a7180-103">IAgentCharacter :: est à obtenir</span><span class="sxs-lookup"><span data-stu-id="a7180-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="a7180-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7180-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="a7180-105">Récupère la taille du frame d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="a7180-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="a7180-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a7180-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a7180-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="a7180-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="a7180-108">Adresse d’une variable qui reçoit la largeur du cadre d’animation de caractères en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="a7180-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a7180-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="a7180-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="a7180-110">Adresse d’une variable qui reçoit la hauteur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="a7180-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="a7180-111">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="a7180-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7180-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7180-112">See Also</span></span>

[<span data-ttu-id="a7180-113">**IAgentCharacter :: configure**</span><span class="sxs-lookup"><span data-stu-id="a7180-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 





---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028990"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="39fe3-103">IAgentCharacter :: SetPosition</span><span class="sxs-lookup"><span data-stu-id="39fe3-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="39fe3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39fe3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="39fe3-105">Définit la position du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="39fe3-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="39fe3-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="39fe3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="39fe3-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span><span class="sxs-lookup"><span data-stu-id="39fe3-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="39fe3-108">Coordonnée d’écran du bord gauche du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="39fe3-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="39fe3-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span><span class="sxs-lookup"><span data-stu-id="39fe3-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="39fe3-110">Coordonnée d’écran du bord supérieur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="39fe3-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="39fe3-111">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="39fe3-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="39fe3-112">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="39fe3-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="39fe3-113">Contrairement à la méthode [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , cette fonction n’est pas mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="39fe3-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="39fe3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39fe3-114">See Also</span></span>

[<span data-ttu-id="39fe3-115">**IAgentCharacter :: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="39fe3-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 





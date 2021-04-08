---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674990"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="0a6bb-103">IAgentCharacter :: configure</span><span class="sxs-lookup"><span data-stu-id="0a6bb-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="0a6bb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a6bb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="0a6bb-105">Définit la taille du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="0a6bb-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0a6bb-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="0a6bb-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="0a6bb-108">Largeur, en pixels, du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0a6bb-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="0a6bb-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="0a6bb-110">Hauteur, en pixels, du cadre d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="0a6bb-111">La modification de la taille du cadre du caractère met à l’échelle le caractère sur la taille définie avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="0a6bb-112">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="0a6bb-113">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="0a6bb-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a6bb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a6bb-114">See Also</span></span>

[<span data-ttu-id="0a6bb-115">**IAgentCharacter :: est à obtenir**</span><span class="sxs-lookup"><span data-stu-id="0a6bb-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 





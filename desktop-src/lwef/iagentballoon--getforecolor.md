---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511640"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="65aa1-103">IAgentBalloon::GetForeColor</span><span class="sxs-lookup"><span data-stu-id="65aa1-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="65aa1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65aa1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="65aa1-105">Récupère la valeur de la couleur de premier plan affichée dans une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="65aa1-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="65aa1-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="65aa1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="65aa1-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span><span class="sxs-lookup"><span data-stu-id="65aa1-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="65aa1-108">Adresse d’une variable qui reçoit le paramètre de couleur pour le premier plan de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="65aa1-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="65aa1-109">La couleur de premier plan utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="65aa1-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="65aa1-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="65aa1-110">It cannot be changed by an application.</span></span> <span data-ttu-id="65aa1-111">Toutefois, l’utilisateur peut remplacer la couleur de premier plan des bulles de mot pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="65aa1-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="65aa1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65aa1-112">See Also</span></span>

[<span data-ttu-id="65aa1-113">**IAgentBalloon::GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="65aa1-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 





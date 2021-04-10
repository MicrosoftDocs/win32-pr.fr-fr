---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674230"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="3cebb-103">IAgentBalloon::GetBorderColor</span><span class="sxs-lookup"><span data-stu-id="3cebb-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="3cebb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cebb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="3cebb-105">Récupère la valeur de la couleur de bordure affichée pour une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="3cebb-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="3cebb-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3cebb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3cebb-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span><span class="sxs-lookup"><span data-stu-id="3cebb-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="3cebb-108">Adresse d’une variable qui reçoit le paramètre de couleur pour la bordure de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3cebb-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="3cebb-109">La couleur de bordure d’une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3cebb-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3cebb-110">Elle ne peut pas être modifiée par une application.</span><span class="sxs-lookup"><span data-stu-id="3cebb-110">It cannot be changed by an application.</span></span> <span data-ttu-id="3cebb-111">Toutefois, l’utilisateur peut modifier la couleur de bordure des bulles de mot pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3cebb-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cebb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cebb-112">See Also</span></span>

<span data-ttu-id="3cebb-113">[**IAgentBalloon :: getBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon :: getForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="3cebb-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 





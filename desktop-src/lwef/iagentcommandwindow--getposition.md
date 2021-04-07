---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940050"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="60fc9-103">IAgentCommandWindow :: GetPosition</span><span class="sxs-lookup"><span data-stu-id="60fc9-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="60fc9-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60fc9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="60fc9-105">Récupère la position de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="60fc9-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="60fc9-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="60fc9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="60fc9-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="60fc9-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="60fc9-108">Adresse d’une variable qui reçoit la coordonnée d’écran du bord gauche de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="60fc9-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="60fc9-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="60fc9-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="60fc9-110">Adresse d’une variable qui reçoit la coordonnée d’écran du bord supérieur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="60fc9-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="60fc9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60fc9-111">See Also</span></span>

[<span data-ttu-id="60fc9-112">**IAgentCommandWindow :: est à obtenir**</span><span class="sxs-lookup"><span data-stu-id="60fc9-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 





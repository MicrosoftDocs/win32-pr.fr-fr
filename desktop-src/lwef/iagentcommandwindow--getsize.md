---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509202"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="6befe-103">IAgentCommandWindow :: est à obtenir</span><span class="sxs-lookup"><span data-stu-id="6befe-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="6befe-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6befe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="6befe-105">Récupère la taille actuelle de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="6befe-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="6befe-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6befe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6befe-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="6befe-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="6befe-108">Adresse d’une variable qui reçoit la largeur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="6befe-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="6befe-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="6befe-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="6befe-110">Adresse d’une variable qui reçoit la hauteur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="6befe-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6befe-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6befe-111">See Also</span></span>

[<span data-ttu-id="6befe-112">**IAgentCommandWindow :: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="6befe-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 





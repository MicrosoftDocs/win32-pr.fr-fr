---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511019"
---
# <a name="iagentballoonsetvisible"></a><span data-ttu-id="cd7fb-103">IAgentBalloon :: SetVisible</span><span class="sxs-lookup"><span data-stu-id="cd7fb-103">IAgentBalloon::SetVisible</span></span>

<span data-ttu-id="cd7fb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd7fb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

<span data-ttu-id="cd7fb-105">Définit la propriété [**visible**](visible-property.md) pour le mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-105">Sets the [**Visible**](visible-property.md) property for the word balloon.</span></span>

-   <span data-ttu-id="cd7fb-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cd7fb-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="cd7fb-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="cd7fb-108">Paramètre de propriété visible.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-108">Visible property setting.</span></span> <span data-ttu-id="cd7fb-109">La valeur **true** affiche le mot-bulle. la valeur **false** le masque.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-109">A value of **True** displays the word balloon; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="cd7fb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd7fb-110">See Also</span></span>

[<span data-ttu-id="cd7fb-111">**IAgentBalloon::GetVisible**</span><span class="sxs-lookup"><span data-stu-id="cd7fb-111">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 





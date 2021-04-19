---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511009"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="4b98d-103">IAgentCommandWindow::GetVisible</span><span class="sxs-lookup"><span data-stu-id="4b98d-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="4b98d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b98d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="4b98d-105">Détermine si la fenêtre commandes vocales est visible ou masquée.</span><span class="sxs-lookup"><span data-stu-id="4b98d-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="4b98d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4b98d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4b98d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="4b98d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="4b98d-108">Adresse d’une variable qui reçoit la **valeur true** si la fenêtre commandes vocales est visible, ou **false** si elle est masquée.</span><span class="sxs-lookup"><span data-stu-id="4b98d-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4b98d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b98d-109">See Also</span></span>

[<span data-ttu-id="4b98d-110">**IAgentCommandWindow :: SetVisible**</span><span class="sxs-lookup"><span data-stu-id="4b98d-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 





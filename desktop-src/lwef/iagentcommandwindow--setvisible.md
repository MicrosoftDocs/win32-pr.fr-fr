---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029406"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="70478-103">IAgentCommandWindow :: SetVisible</span><span class="sxs-lookup"><span data-stu-id="70478-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="70478-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70478-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="70478-105">Définissez la propriété [**visible**](visible-property.md) pour la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="70478-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="70478-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="70478-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="70478-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="70478-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="70478-108">Paramètre de propriété [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="70478-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="70478-109">La valeur **true** affiche la fenêtre commandes vocales. **False** le masque.</span><span class="sxs-lookup"><span data-stu-id="70478-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="70478-110">L’utilisateur peut remplacer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="70478-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="70478-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70478-111">See Also</span></span>

[<span data-ttu-id="70478-112">**IAgentCommandWindow::GetVisible**</span><span class="sxs-lookup"><span data-stu-id="70478-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 





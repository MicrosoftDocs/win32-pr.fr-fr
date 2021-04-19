---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511687"
---
# <a name="iagentcommandsgetvisible"></a><span data-ttu-id="e8b26-103">IAgentCommands::GetVisible</span><span class="sxs-lookup"><span data-stu-id="e8b26-103">IAgentCommands::GetVisible</span></span>

<span data-ttu-id="e8b26-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8b26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

<span data-ttu-id="e8b26-105">Récupère la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e8b26-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e8b26-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e8b26-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e8b26-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="e8b26-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="e8b26-108">Adresse d’une variable qui reçoit la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e8b26-108">The address of a variable that receives the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e8b26-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8b26-109">See Also</span></span>

<span data-ttu-id="e8b26-110">[**IAgentCommands :: setVisible**](iagentcommands--setvisible.md), [ **IAgentCommands :: SetCaption**](iagentcommands--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="e8b26-110">[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md)</span></span>


 

 
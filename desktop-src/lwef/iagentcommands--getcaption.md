---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509026"
---
# <a name="iagentcommandsgetcaption"></a><span data-ttu-id="117dd-103">IAgentCommands::GetCaption</span><span class="sxs-lookup"><span data-stu-id="117dd-103">IAgentCommands::GetCaption</span></span>

<span data-ttu-id="117dd-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="117dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

<span data-ttu-id="117dd-105">Récupère la [**légende**](caption-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="117dd-105">Retrieves the [**Caption**](caption-property.md) for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="117dd-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="117dd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="117dd-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span><span class="sxs-lookup"><span data-stu-id="117dd-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="117dd-108">Adresse d’un BSTR qui reçoit la valeur du paramètre de texte de [**légende**](caption-property.md) affiché pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="117dd-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text setting displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="117dd-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="117dd-109">See Also</span></span>

<span data-ttu-id="117dd-110">[**IAgentCommands :: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands :: getVisible**](iagentcommands--getvisible.md), [**IAgentCommands :: GetVoice**](iagentcommands--getvoice.md)</span><span class="sxs-lookup"><span data-stu-id="117dd-110">[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)</span></span>


 

 
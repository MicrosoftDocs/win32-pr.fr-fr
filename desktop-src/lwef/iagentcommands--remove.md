---
title: IAgentCommands supprimer
description: IAgentCommands supprimer
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198962"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="e0abe-103">IAgentCommands :: Remove</span><span class="sxs-lookup"><span data-stu-id="e0abe-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="e0abe-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0abe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="e0abe-105">Supprime la [**commande**](/windows/desktop/lwef/the-command-object) spécifiée d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e0abe-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e0abe-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e0abe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e0abe-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="e0abe-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="e0abe-108">ID d’une [**commande**](/windows/desktop/lwef/the-command-object) à supprimer de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e0abe-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="e0abe-109">La suppression d’une [**commande**](/windows/desktop/lwef/the-command-object) d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) la supprime également du menu contextuel et de la **fenêtre commandes vocales** lorsque votre application est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="e0abe-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0abe-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0abe-110">See Also</span></span>

<span data-ttu-id="e0abe-111">[**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommands :: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="e0abe-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 
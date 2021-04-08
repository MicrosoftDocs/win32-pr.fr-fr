---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727037"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="45c67-103">IAgentCommands :: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="45c67-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="45c67-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45c67-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="45c67-105">Supprime toutes les [**commandes**](/windows/desktop/lwef/the-command-object) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="45c67-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="45c67-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="45c67-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="45c67-107">La suppression de toutes les [**commandes**](/windows/desktop/lwef/the-command-object) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) les supprime également du menu contextuel et de la **fenêtre commandes vocales** lorsque votre application est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="45c67-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="45c67-108">**RemoveAll** ne supprime pas les entrées du serveur ou d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="45c67-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="45c67-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45c67-109">See Also</span></span>

<span data-ttu-id="45c67-110">[**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommands :: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="45c67-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 
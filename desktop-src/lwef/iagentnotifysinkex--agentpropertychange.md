---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939975"
---
# <a name="iagentnotifysinkexagentpropertychange"></a><span data-ttu-id="e2ed2-103">IAgentNotifySinkEx::AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="e2ed2-103">IAgentNotifySinkEx::AgentPropertyChange</span></span>

<span data-ttu-id="e2ed2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2ed2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AgentPropertyChange(
);
```

<span data-ttu-id="e2ed2-105">Avertit une application cliente lorsque l’utilisateur modifie un paramètre de propriété de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2ed2-105">Notifies a client application when the user changes a Microsoft Agent property setting.</span></span>

-   <span data-ttu-id="e2ed2-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e2ed2-106">No return value.</span></span>

<span data-ttu-id="e2ed2-107">Lorsque l’utilisateur modifie un paramètre de propriété de l’agent Microsoft dans la feuille de propriétés de l’agent Microsoft, le serveur envoie cet événement à tous les clients, sauf si le serveur est actuellement suspendu.</span><span class="sxs-lookup"><span data-stu-id="e2ed2-107">When the user changes a Microsoft Agent property setting in the Microsoft Agent property sheet, the server sends this event to all clients unless the server is currently suspended.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2ed2-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2ed2-108">See Also</span></span>

[<span data-ttu-id="e2ed2-109">**IAgentNotifySinkEx ::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="e2ed2-109">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 





---
title: IAgentNotifySink inactif
description: IAgentNotifySink inactif
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512687"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="185f9-103">IAgentNotifySink :: Idle</span><span class="sxs-lookup"><span data-stu-id="185f9-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="185f9-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="185f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="185f9-105">Avertit une application cliente lorsque l’état de **ralenti** d’un caractère a changé.</span><span class="sxs-lookup"><span data-stu-id="185f9-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="185f9-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="185f9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="185f9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="185f9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="185f9-108">Identificateur de la demande qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="185f9-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="185f9-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bDémarrer*</span><span class="sxs-lookup"><span data-stu-id="185f9-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="185f9-110">Indicateur de début.</span><span class="sxs-lookup"><span data-stu-id="185f9-110">Start flag.</span></span> <span data-ttu-id="185f9-111">Cette valeur booléenne est **true** lorsque le caractère commence le ralenti et **false** lorsqu’il arrête le ralenti.</span><span class="sxs-lookup"><span data-stu-id="185f9-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="185f9-112">Cet événement vous permet de suivre le moment où le serveur Microsoft Agent démarre ou arrête le traitement de l’inactivité d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="185f9-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="185f9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="185f9-113">See Also</span></span>

<span data-ttu-id="185f9-114">[**IAgentCharacter :: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter :: SetIdleOn**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="185f9-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 





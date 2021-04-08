---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675281"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="32e89-103">IAgentNotifySink::RequestStart</span><span class="sxs-lookup"><span data-stu-id="32e89-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="32e89-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32e89-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="32e89-105">Avertit une application cliente qu’une demande commence.</span><span class="sxs-lookup"><span data-stu-id="32e89-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="32e89-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="32e89-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="32e89-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="32e89-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="32e89-108">Identificateur de la demande qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="32e89-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="32e89-109">Cet événement vous permet de suivre le moment où une demande en file d’attente commence à utiliser son ID de demande.</span><span class="sxs-lookup"><span data-stu-id="32e89-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="32e89-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e89-110">See Also</span></span>

<span data-ttu-id="32e89-111">[**IAgentNotifySink :: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent :: Load**](iagent--load.md), [**IAgentCharacter :: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter :: Hide**](iagentcharacter--hide.md), [**IAgentCharacter :: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md)res, [**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentCharacter :: Show**](iagentcharacter--show.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [**IAgentCharacter :: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="32e89-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 





---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311041"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="52e37-103">IAgentNotifySink::RequestComplete</span><span class="sxs-lookup"><span data-stu-id="52e37-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="52e37-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52e37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="52e37-105">Avertit une application cliente quand une demande est terminée.</span><span class="sxs-lookup"><span data-stu-id="52e37-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="52e37-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="52e37-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="52e37-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="52e37-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="52e37-108">Identificateur de la demande qui a démarré.</span><span class="sxs-lookup"><span data-stu-id="52e37-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="52e37-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="52e37-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="52e37-110">Code d’état.</span><span class="sxs-lookup"><span data-stu-id="52e37-110">Status code.</span></span> <span data-ttu-id="52e37-111">Ce paramètre retourne le code d’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="52e37-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="52e37-112">Cet événement vous permet de suivre le moment où une méthode en file d’attente se termine à l’aide de son ID de demande.</span><span class="sxs-lookup"><span data-stu-id="52e37-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="52e37-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52e37-113">See Also</span></span>

<span data-ttu-id="52e37-114">[**IAgentNotifySink :: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent :: Load**](iagent--load.md), [**IAgentCharacter :: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter :: Hide**](iagentcharacter--hide.md), [**IAgentCharacter :: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md)res, [**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentCharacter :: Show**](iagentcharacter--show.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md), [**IAgentCharacter :: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="52e37-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 





---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507275"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="cc861-103">IAgentNotifySinkEx::ListeningState</span><span class="sxs-lookup"><span data-stu-id="cc861-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="cc861-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc861-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="cc861-105">Avertit une application cliente lorsque le mode d’écoute change.</span><span class="sxs-lookup"><span data-stu-id="cc861-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="cc861-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cc861-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cc861-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span><span class="sxs-lookup"><span data-stu-id="cc861-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="cc861-108">Caractère pour lequel l’état d’écoute a changé.</span><span class="sxs-lookup"><span data-stu-id="cc861-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="cc861-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span><span class="sxs-lookup"><span data-stu-id="cc861-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="cc861-110">État du mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="cc861-110">The Listening mode state.</span></span> <span data-ttu-id="cc861-111">**True** indique que le mode d’écoute a démarré ; **False**, ce mode d’écoute est terminé.</span><span class="sxs-lookup"><span data-stu-id="cc861-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="cc861-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="cc861-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="cc861-113">La cause de l’événement, qui peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc861-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="cc861-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc861-114">Value</span></span>                                                                             | <span data-ttu-id="cc861-115">Description</span><span class="sxs-lookup"><span data-stu-id="cc861-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cc861-116">**const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMDISABLED = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="cc861-117">Le mode d’écoute a été désactivé par le code de programme.</span><span class="sxs-lookup"><span data-stu-id="cc861-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="cc861-118">**const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMTIMEDOUT = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="cc861-119">Le mode d’écoute (activé par code de programme) a expiré.</span><span class="sxs-lookup"><span data-stu-id="cc861-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="cc861-120">**const unsigned long** **LSCOMPLETE \_ cause \_ USERTIMEDOUT = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="cc861-121">Le mode d’écoute (activé par la clé d’écoute) a expiré.</span><span class="sxs-lookup"><span data-stu-id="cc861-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="cc861-122">**const unsigned long** **LSCOMPLETE \_ cause \_ USERRELEASEDKEY = 4 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="cc861-123">Le mode d’écoute a été désactivé, car l’utilisateur a relâché la clé d’écoute.</span><span class="sxs-lookup"><span data-stu-id="cc861-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="cc861-124">**const unsigned long** **LSCOMPLETE \_ cause \_ USERUTTERANCEENDED = 5 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="cc861-125">Le mode d’écoute a été désactivé, car l’utilisateur a terminé de parler.</span><span class="sxs-lookup"><span data-stu-id="cc861-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="cc861-126">**const unsigned long** **LSCOMPLETE \_ cause \_ CLIENTDEACTIVATED = 6 ;**</span><span class="sxs-lookup"><span data-stu-id="cc861-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="cc861-127">Le mode d’écoute a été désactivé, car le client actif d’entrée a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="cc861-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="cc861-128">**const unsigned long** **LSCOMPLETE \_ cause \_ DEFAULTCHARCHANGE = 7**</span><span class="sxs-lookup"><span data-stu-id="cc861-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="cc861-129">Le mode d’écoute a été désactivé car le caractère par défaut a été modifié.</span><span class="sxs-lookup"><span data-stu-id="cc861-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="cc861-130">**const unsigned long** **LSCOMPLETE \_ cause \_ USERDISABLED = 8**</span><span class="sxs-lookup"><span data-stu-id="cc861-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="cc861-131">Le mode d’écoute a été désactivé, car l’utilisateur a désactivé l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="cc861-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="cc861-132">Cet événement est envoyé à tous les clients lorsque le mode d’écoute commence après que l’utilisateur appuie sur la touche d’écoute ou à la fin de son délai d’attente, ou lorsque le client d’entrée-actif appelle la méthode [**IAgentCharacterEx :: Listen**](iagentcharacterex--listen.md) avec **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="cc861-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="cc861-133">L’événement retourne des valeurs aux clients pour lesquels ce caractère est actuellement chargé.</span><span class="sxs-lookup"><span data-stu-id="cc861-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="cc861-134">Tous les autres clients reçoivent un caractère null (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="cc861-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc861-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc861-135">See Also</span></span>

[<span data-ttu-id="cc861-136">**IAgentCharacterEx :: Listen**</span><span class="sxs-lookup"><span data-stu-id="cc861-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 






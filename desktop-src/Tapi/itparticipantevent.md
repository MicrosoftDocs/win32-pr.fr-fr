---
description: L’interface ITParticipantEvent contient des méthodes qui récupèrent la description des événements participant.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interface ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525500"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="1bc7a-103">Interface ITParticipantEvent</span><span class="sxs-lookup"><span data-stu-id="1bc7a-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="1bc7a-104">\[**ITParticipantEvent** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1bc7a-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1bc7a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1bc7a-106">L’interface **ITParticipantEvent** contient des méthodes qui récupèrent la description des événements participant.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="1bc7a-107">Lorsque l’implémentation de l’application de la méthode [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indique qu’un [**\_ événement TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) est égal à **te \_ Private**, le paramètre *pEvent* de la méthode est un pointeur **IDispatch** pour l’interface **ITParticipantEvent** .</span><span class="sxs-lookup"><span data-stu-id="1bc7a-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="1bc7a-108">Les méthodes de cette interface peuvent être utilisées pour récupérer des informations concernant une modification de participant qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="1bc7a-109">Vous devez appeler la méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) et définir un masque de filtre d’événement qui comprend l’événement **\_ Private te** pour activer la réception des événements participant.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="1bc7a-110">Si vous n’appelez pas **ITTAPI ::p ut \_ EventFilter**, votre application ne recevra aucun événement.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="1bc7a-111">Pour plus d’informations, consultez la vue d’ensemble des [événements](events.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc7a-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="1bc7a-112">Membres</span><span class="sxs-lookup"><span data-stu-id="1bc7a-112">Members</span></span>

<span data-ttu-id="1bc7a-113">L’interface **ITParticipantEvent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1bc7a-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1bc7a-114">**ITParticipantEvent** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1bc7a-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="1bc7a-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1bc7a-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1bc7a-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1bc7a-116">Methods</span></span>

<span data-ttu-id="1bc7a-117">L’interface **ITParticipantEvent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="1bc7a-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="1bc7a-118">Method</span></span>                                                         | <span data-ttu-id="1bc7a-119">Description</span><span class="sxs-lookup"><span data-stu-id="1bc7a-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bc7a-120">**recevoir un \_ événement**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="1bc7a-121">Obtient le descripteur d' [**\_ événement participant**](participant-event.md) de l’événement.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="1bc7a-122">**recevoir un \_ participant**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="1bc7a-123">Obtient un pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) représentant les participants impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="1bc7a-124">**extraire le sous- \_ flux**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="1bc7a-125">Obtient un pointeur vers un tableau d’interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) représentant les sous-flux impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="1bc7a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bc7a-126">Requirements</span></span>



| <span data-ttu-id="1bc7a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bc7a-127">Requirement</span></span> | <span data-ttu-id="1bc7a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc7a-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc7a-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="1bc7a-129">TAPI version</span></span><br/> | <span data-ttu-id="1bc7a-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1bc7a-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1bc7a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bc7a-131">Header</span></span><br/>       | <dl> <span data-ttu-id="1bc7a-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7a-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="1bc7a-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bc7a-133">Library</span></span><br/>      | <dl> <span data-ttu-id="1bc7a-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7a-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1bc7a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc7a-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="1bc7a-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7a-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1bc7a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc7a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc7a-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="1bc7a-139">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="1bc7a-140">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="1bc7a-141">**\_événement participant**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="1bc7a-142">**ITTAPIEventNotification :: Event**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="1bc7a-143">**\_événement TAPI**</span><span class="sxs-lookup"><span data-stu-id="1bc7a-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="1bc7a-144">Enregistrer l’extrait de code des événements</span><span class="sxs-lookup"><span data-stu-id="1bc7a-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 


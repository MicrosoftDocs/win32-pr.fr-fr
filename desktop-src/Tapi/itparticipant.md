---
description: L’interface ITParticipant est implémentée par le MSP IPConf. Il permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interface ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544035"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="1943c-104">Interface ITParticipant</span><span class="sxs-lookup"><span data-stu-id="1943c-104">ITParticipant interface</span></span>

<span data-ttu-id="1943c-105">\[**ITParticipant** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1943c-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1943c-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1943c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1943c-107">L’interface **ITParticipant** est implémentée par le [MSP ipconf](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="1943c-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="1943c-108">Il permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.</span><span class="sxs-lookup"><span data-stu-id="1943c-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="1943c-109">Cette interface est exposée sur l’objet d’appel lorsqu’un appel utilise la conférence IP.</span><span class="sxs-lookup"><span data-stu-id="1943c-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="1943c-110">Un pointeur peut être obtenu en appelant **QueryInterface** à l’aide d’un pointeur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="1943c-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="1943c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1943c-111">Members</span></span>

<span data-ttu-id="1943c-112">L’interface **ITParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1943c-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1943c-113">**ITParticipant** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1943c-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="1943c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1943c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1943c-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1943c-115">Methods</span></span>

<span data-ttu-id="1943c-116">L’interface **ITParticipant** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1943c-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="1943c-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="1943c-117">Method</span></span>                                                                      | <span data-ttu-id="1943c-118">Description</span><span class="sxs-lookup"><span data-stu-id="1943c-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1943c-119">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="1943c-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="1943c-120">Énumère les flux associés au participant actuel.</span><span class="sxs-lookup"><span data-stu-id="1943c-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="1943c-121">**Obtient \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="1943c-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="1943c-122">Obtient les [**types de média**](tapimediatype--constants.md) associés à un participant.</span><span class="sxs-lookup"><span data-stu-id="1943c-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="1943c-123">**Obtient \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="1943c-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="1943c-124">Obtient une représentation BSTR du type d’information nécessaire, par exemple PTI \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="1943c-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="1943c-125">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="1943c-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="1943c-126">Obtient l’état du participant.</span><span class="sxs-lookup"><span data-stu-id="1943c-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="1943c-127">**recevoir des \_ flux**</span><span class="sxs-lookup"><span data-stu-id="1943c-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="1943c-128">Crée une collection de flux associés au participant actuel.</span><span class="sxs-lookup"><span data-stu-id="1943c-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="1943c-129">Fourni pour les applications clientes Automation, telles que celles écrites en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1943c-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="1943c-130">**Placer l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="1943c-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="1943c-131">Définit si un flux associé au participant est activé.</span><span class="sxs-lookup"><span data-stu-id="1943c-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="1943c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1943c-132">Requirements</span></span>



| <span data-ttu-id="1943c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1943c-133">Requirement</span></span> | <span data-ttu-id="1943c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1943c-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1943c-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="1943c-135">TAPI version</span></span><br/> | <span data-ttu-id="1943c-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1943c-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="1943c-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1943c-137">Header</span></span><br/>       | <dl> <span data-ttu-id="1943c-138"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1943c-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1943c-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1943c-139">Library</span></span><br/>      | <dl> <span data-ttu-id="1943c-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1943c-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="1943c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1943c-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="1943c-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1943c-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1943c-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1943c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1943c-144">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="1943c-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="1943c-145">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="1943c-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1943c-146">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="1943c-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 


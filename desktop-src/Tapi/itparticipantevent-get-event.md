---
description: La \_ méthode d’événement obtenir obtient un \_ descripteur d’événement participant du type d’événement qui s’est produit.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'ITParticipantEvent :: get_Event, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544484"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="bffce-103">ITParticipantEvent :: acobtiens, \_ méthode d’événement</span><span class="sxs-lookup"><span data-stu-id="bffce-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="bffce-104">\[en **savoir \_ plus L’événement** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bffce-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bffce-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bffce-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bffce-106">La méthode d' **\_ événement obtenir** obtient un descripteur d' [**\_ événement participant**](participant-event.md) du type d’événement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="bffce-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bffce-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="bffce-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bffce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffce-109">*pParticipantEvent* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bffce-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bffce-110">Pointeur vers le descripteur d' [**\_ événement participant**](participant-event.md) de l’événement.</span><span class="sxs-lookup"><span data-stu-id="bffce-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffce-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bffce-111">Return value</span></span>

<span data-ttu-id="bffce-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="bffce-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bffce-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bffce-113">Value</span></span>                                                                                         | <span data-ttu-id="bffce-114">Signification</span><span class="sxs-lookup"><span data-stu-id="bffce-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="bffce-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bffce-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="bffce-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="bffce-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bffce-118">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bffce-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="bffce-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bffce-120">Le paramètre *pParticipantEvent* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="bffce-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bffce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bffce-121">Requirements</span></span>



| <span data-ttu-id="bffce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bffce-122">Requirement</span></span> | <span data-ttu-id="bffce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bffce-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bffce-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bffce-124">TAPI version</span></span><br/> | <span data-ttu-id="bffce-125">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bffce-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bffce-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="bffce-126">Header</span></span><br/>       | <dl> <span data-ttu-id="bffce-127"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="bffce-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bffce-128">Library</span></span><br/>      | <dl> <span data-ttu-id="bffce-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bffce-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bffce-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="bffce-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bffce-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bffce-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bffce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffce-133">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="bffce-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="bffce-134">**\_événement participant**</span><span class="sxs-lookup"><span data-stu-id="bffce-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 





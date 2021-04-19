---
description: La méthode obtenir le \_ participant obtient un pointeur vers un tableau d’interfaces ITParticipant représentant les participants impliqués dans l’événement.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'ITParticipantEvent :: get_Participant, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537538"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="10413-103">ITParticipantEvent :: obtient la \_ méthode participante</span><span class="sxs-lookup"><span data-stu-id="10413-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="10413-104">\[en **savoir \_ plus Le participant** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="10413-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="10413-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="10413-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="10413-106">La méthode **obtenir le \_ participant** obtient un pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) représentant les participants impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="10413-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="10413-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10413-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="10413-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10413-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10413-109">*ppParticipant* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="10413-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10413-110">Pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="10413-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10413-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10413-111">Return value</span></span>

<span data-ttu-id="10413-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="10413-112">This method can return one of these values.</span></span>



| <span data-ttu-id="10413-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="10413-113">Value</span></span>                                                                                           | <span data-ttu-id="10413-114">Signification</span><span class="sxs-lookup"><span data-stu-id="10413-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="10413-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10413-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="10413-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="10413-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="10413-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="10413-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="10413-118">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="10413-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="10413-119"><dt>**\_NOitems TAPI E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10413-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="10413-120">Aucun participant n’est associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="10413-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="10413-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="10413-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="10413-122">Le paramètre *ppParticipant* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="10413-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="10413-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10413-123">Requirements</span></span>



| <span data-ttu-id="10413-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10413-124">Requirement</span></span> | <span data-ttu-id="10413-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="10413-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10413-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="10413-126">TAPI version</span></span><br/> | <span data-ttu-id="10413-127">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="10413-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="10413-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="10413-128">Header</span></span><br/>       | <dl> <span data-ttu-id="10413-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="10413-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="10413-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10413-130">Library</span></span><br/>      | <dl> <span data-ttu-id="10413-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10413-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="10413-132">DLL</span><span class="sxs-lookup"><span data-stu-id="10413-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="10413-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10413-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="10413-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10413-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10413-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="10413-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="10413-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="10413-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 





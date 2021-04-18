---
description: La méthode EnumerateParticipants énumère les participants associés à la Conférence en cours.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl :: EnumerateParticipants, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525944"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="14e6f-103">ITParticipantControl :: EnumerateParticipants, méthode</span><span class="sxs-lookup"><span data-stu-id="14e6f-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="14e6f-104">\[**EnumerateParticipants** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="14e6f-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14e6f-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="14e6f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14e6f-106">La méthode **EnumerateParticipants** énumère les participants associés à la Conférence en cours.</span><span class="sxs-lookup"><span data-stu-id="14e6f-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="14e6f-107">Cette méthode est fournie pour les applications C et C++.</span><span class="sxs-lookup"><span data-stu-id="14e6f-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="14e6f-108">Les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la méthode d' [**extraction des \_ participants**](itparticipantcontrol-get-participants.md) .</span><span class="sxs-lookup"><span data-stu-id="14e6f-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e6f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14e6f-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="14e6f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14e6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e6f-111">*ppEnumParticipants* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14e6f-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14e6f-112">Pointeur vers l’interface [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="14e6f-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e6f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14e6f-113">Return value</span></span>

<span data-ttu-id="14e6f-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="14e6f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="14e6f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e6f-115">Value</span></span>                                                                                         | <span data-ttu-id="14e6f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="14e6f-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="14e6f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="14e6f-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="14e6f-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="14e6f-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="14e6f-120">Le paramètre *ppEnumParticipants* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="14e6f-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="14e6f-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="14e6f-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="14e6f-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="14e6f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="14e6f-123">Remarks</span></span>

<span data-ttu-id="14e6f-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumParticipant**](ienumparticipant.md) retournée par **ITParticipantControl :: EnumerateParticipants**.</span><span class="sxs-lookup"><span data-stu-id="14e6f-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="14e6f-125">L’application doit appeler **Release** sur l’interface **IEnumParticipant** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="14e6f-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e6f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14e6f-126">Requirements</span></span>



| <span data-ttu-id="14e6f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14e6f-127">Requirement</span></span> | <span data-ttu-id="14e6f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e6f-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14e6f-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="14e6f-129">TAPI version</span></span><br/> | <span data-ttu-id="14e6f-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="14e6f-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="14e6f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="14e6f-131">Header</span></span><br/>       | <dl> <span data-ttu-id="14e6f-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="14e6f-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14e6f-133">Library</span></span><br/>      | <dl> <span data-ttu-id="14e6f-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="14e6f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="14e6f-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="14e6f-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14e6f-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="14e6f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14e6f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e6f-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="14e6f-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="14e6f-139">**accéder aux \_ participants**</span><span class="sxs-lookup"><span data-stu-id="14e6f-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="14e6f-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="14e6f-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="14e6f-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="14e6f-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 





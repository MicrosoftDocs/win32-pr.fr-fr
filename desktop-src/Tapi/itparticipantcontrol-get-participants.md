---
description: La \_ méthode obtenir des participants crée une collection de participants associés à la Conférence en cours.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'ITParticipantControl :: get_Participants, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542332"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="86c51-103">ITParticipantControl :: obtient la \_ méthode des participants</span><span class="sxs-lookup"><span data-stu-id="86c51-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="86c51-104">\[en **savoir \_ plus Les participants** ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="86c51-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86c51-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="86c51-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86c51-106">La méthode **obtenir des \_ participants** crée une collection de participants associés à la Conférence en cours.</span><span class="sxs-lookup"><span data-stu-id="86c51-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="86c51-107">Cette méthode est fournie pour les applications clientes Automation, telles que celles écrites en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="86c51-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="86c51-108">Les applications C et C++ doivent utiliser la méthode [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .</span><span class="sxs-lookup"><span data-stu-id="86c51-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c51-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86c51-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="86c51-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86c51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c51-111">*pVariant* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86c51-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c51-112">Pointeur vers un **Variant** contenant un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de pointeurs d’interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="86c51-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c51-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86c51-113">Return value</span></span>

<span data-ttu-id="86c51-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="86c51-114">This method can return one of these values.</span></span>



| <span data-ttu-id="86c51-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86c51-115">Value</span></span>                                                                                         | <span data-ttu-id="86c51-116">Signification</span><span class="sxs-lookup"><span data-stu-id="86c51-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="86c51-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86c51-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="86c51-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="86c51-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86c51-120">Le paramètre *pVariant* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="86c51-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="86c51-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86c51-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="86c51-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86c51-123">Notes</span><span class="sxs-lookup"><span data-stu-id="86c51-123">Remarks</span></span>

<span data-ttu-id="86c51-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITParticipant**](itparticipant.md) retournée par **ITParticipantControl :: obtient \_ participants**.</span><span class="sxs-lookup"><span data-stu-id="86c51-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="86c51-125">L’application doit appeler **Release** sur l’interface **ITParticipant** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="86c51-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c51-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c51-126">Requirements</span></span>



| <span data-ttu-id="86c51-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86c51-127">Requirement</span></span> | <span data-ttu-id="86c51-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="86c51-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86c51-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="86c51-129">TAPI version</span></span><br/> | <span data-ttu-id="86c51-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="86c51-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86c51-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="86c51-131">Header</span></span><br/>       | <dl> <span data-ttu-id="86c51-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="86c51-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86c51-133">Library</span></span><br/>      | <dl> <span data-ttu-id="86c51-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86c51-135">DLL</span><span class="sxs-lookup"><span data-stu-id="86c51-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="86c51-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c51-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="86c51-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c51-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c51-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="86c51-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="86c51-139">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="86c51-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="86c51-140">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="86c51-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="86c51-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="86c51-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 





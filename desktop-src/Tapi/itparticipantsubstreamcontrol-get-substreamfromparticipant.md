---
description: La \_ méthode obtenir SubStreamFromParticipant permet à une application de détecter les sous-flux associés à un participant donné.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'ITParticipantSubStreamControl :: get_SubStreamFromParticipant, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526697"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="a81f0-103">ITParticipantSubStreamControl :: \_ SubStreamFromParticipant, méthode</span><span class="sxs-lookup"><span data-stu-id="a81f0-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="a81f0-104">\[en **savoir \_ plus SubStreamFromParticipant** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a81f0-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a81f0-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a81f0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a81f0-106">La méthode **obtenir \_ SubStreamFromParticipant** permet à une application de détecter les sous-flux associés à un participant donné.</span><span class="sxs-lookup"><span data-stu-id="a81f0-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a81f0-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="a81f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a81f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a81f0-109">*pParticipant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a81f0-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a81f0-110">Pointeur vers l’interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="a81f0-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a81f0-111">*ppITSubStream* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a81f0-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a81f0-112">Pointeur vers un tableau de pointeurs d’interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="a81f0-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a81f0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a81f0-113">Return value</span></span>

<span data-ttu-id="a81f0-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a81f0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a81f0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a81f0-115">Return code</span></span>                                                                                   | <span data-ttu-id="a81f0-116">Description</span><span class="sxs-lookup"><span data-stu-id="a81f0-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a81f0-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a81f0-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a81f0-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="a81f0-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a81f0-120">Le paramètre *ppITSubStream* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a81f0-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="a81f0-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a81f0-122">Le paramètre *pParticipant* ne pointe pas vers une interface valide.</span><span class="sxs-lookup"><span data-stu-id="a81f0-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="a81f0-123"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="a81f0-124">Impossible d’accéder aux informations sur le participant du flux.</span><span class="sxs-lookup"><span data-stu-id="a81f0-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="a81f0-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a81f0-126">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a81f0-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="a81f0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a81f0-127">Requirements</span></span>



| <span data-ttu-id="a81f0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a81f0-128">Requirement</span></span> | <span data-ttu-id="a81f0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a81f0-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a81f0-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a81f0-130">TAPI version</span></span><br/> | <span data-ttu-id="a81f0-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a81f0-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a81f0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a81f0-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a81f0-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="a81f0-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a81f0-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a81f0-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a81f0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a81f0-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a81f0-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a81f0-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a81f0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a81f0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a81f0-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="a81f0-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="a81f0-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="a81f0-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="a81f0-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="a81f0-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 


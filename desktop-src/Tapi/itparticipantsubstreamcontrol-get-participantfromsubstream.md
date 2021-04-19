---
description: La \_ méthode obtenir ParticipantFromSubStream permet à une application de détecter les participants associés à un sous-flux donné.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'ITParticipantSubStreamControl :: get_ParticipantFromSubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544028"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="70252-103">ITParticipantSubStreamControl :: \_ ParticipantFromSubStream, méthode</span><span class="sxs-lookup"><span data-stu-id="70252-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="70252-104">\[en **savoir \_ plus ParticipantFromSubStream** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="70252-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70252-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="70252-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70252-106">La méthode **obtenir \_ ParticipantFromSubStream** permet à une application de détecter les participants associés à un sous-flux donné.</span><span class="sxs-lookup"><span data-stu-id="70252-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="70252-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70252-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="70252-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70252-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70252-109">*pITSubStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70252-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70252-110">Pointeur vers l’interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="70252-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="70252-111">*ppParticipant* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="70252-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70252-112">Pointeur vers un tableau de pointeurs d’interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="70252-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70252-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70252-113">Return value</span></span>

<span data-ttu-id="70252-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="70252-114">This method can return one of these values.</span></span>



| <span data-ttu-id="70252-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="70252-115">Return code</span></span>                                                                                     | <span data-ttu-id="70252-116">Description</span><span class="sxs-lookup"><span data-stu-id="70252-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70252-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70252-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="70252-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="70252-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="70252-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="70252-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="70252-120">Le paramètre *pITSubStream* ou *ppParticipant* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="70252-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="70252-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="70252-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="70252-122">Le paramètre *pITSubStream* ne pointe pas vers une interface valide.</span><span class="sxs-lookup"><span data-stu-id="70252-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="70252-123"><dt>**\_NOitems TAPI E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70252-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="70252-124">Aucun participant n’est associé au sous-flux.</span><span class="sxs-lookup"><span data-stu-id="70252-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="70252-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="70252-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="70252-126">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="70252-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="70252-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70252-127">Requirements</span></span>



| <span data-ttu-id="70252-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70252-128">Requirement</span></span> | <span data-ttu-id="70252-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="70252-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70252-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="70252-130">TAPI version</span></span><br/> | <span data-ttu-id="70252-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="70252-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70252-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="70252-132">Header</span></span><br/>       | <dl> <span data-ttu-id="70252-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="70252-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="70252-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70252-134">Library</span></span><br/>      | <dl> <span data-ttu-id="70252-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70252-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70252-136">DLL</span><span class="sxs-lookup"><span data-stu-id="70252-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="70252-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70252-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="70252-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70252-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70252-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="70252-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="70252-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="70252-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="70252-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="70252-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 


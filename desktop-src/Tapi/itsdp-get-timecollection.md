---
description: La \_ méthode obtenir TimeCollection obtient un pointeur vers une interface ITTimeCollection pour la Conférence.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'ITSdp :: get_TimeCollection, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525542"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="adf29-103">ITSdp :: \_ TimeCollection, méthode</span><span class="sxs-lookup"><span data-stu-id="adf29-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="adf29-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="adf29-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="adf29-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="adf29-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="adf29-106">La méthode **obtenir \_ TimeCollection** obtient un pointeur vers une interface [**ITTimeCollection**](ittimecollection.md) pour la Conférence.</span><span class="sxs-lookup"><span data-stu-id="adf29-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adf29-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="adf29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adf29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf29-109">*ppTimeCollection* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="adf29-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adf29-110">Pointeur vers [**ITTimeCollection**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="adf29-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf29-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adf29-111">Return value</span></span>

<span data-ttu-id="adf29-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="adf29-112">This method can return one of these values.</span></span>



| <span data-ttu-id="adf29-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf29-113">Value</span></span>                                                                                                                           | <span data-ttu-id="adf29-114">Signification</span><span class="sxs-lookup"><span data-stu-id="adf29-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="adf29-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="adf29-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="adf29-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="adf29-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="adf29-118">Le paramètre *ppTimeCollection* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="adf29-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="adf29-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="adf29-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="adf29-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="adf29-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="adf29-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="adf29-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="adf29-123"><dt>**HRESULT \_ à partir du \_ code d’erreur \_ (erreur de \_ données non valides \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="adf29-124">Une erreur interne s’est produite, généralement en raison de l’échec d’une méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="adf29-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="adf29-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="adf29-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="adf29-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="adf29-127">Notes</span><span class="sxs-lookup"><span data-stu-id="adf29-127">Remarks</span></span>

<span data-ttu-id="adf29-128">Un pointeur [**ITTimeCollection**](ittimecollection.md) peut également être obtenu à l’aide de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="adf29-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="adf29-129">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTimeCollection**](ittimecollection.md) retournée par **ITSdp :: \_ TimeCollection**.</span><span class="sxs-lookup"><span data-stu-id="adf29-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="adf29-130">L’application doit appeler **Release** sur l’interface **ITTimeCollection** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="adf29-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf29-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adf29-131">Requirements</span></span>



| <span data-ttu-id="adf29-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adf29-132">Requirement</span></span> | <span data-ttu-id="adf29-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf29-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adf29-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="adf29-134">TAPI version</span></span><br/> | <span data-ttu-id="adf29-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="adf29-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="adf29-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="adf29-136">Header</span></span><br/>       | <dl> <span data-ttu-id="adf29-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="adf29-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adf29-138">Library</span></span><br/>      | <dl> <span data-ttu-id="adf29-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="adf29-140">DLL</span><span class="sxs-lookup"><span data-stu-id="adf29-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="adf29-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf29-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf29-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adf29-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf29-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="adf29-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="adf29-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="adf29-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 





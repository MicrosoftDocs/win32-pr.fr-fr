---
description: La \_ méthode obtenir MediaCollection obtient un pointeur vers l’interface ITMediaCollection pour la Conférence.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'ITSdp :: get_MediaCollection, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525193"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="df8ec-103">ITSdp :: \_ MediaCollection, méthode</span><span class="sxs-lookup"><span data-stu-id="df8ec-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="df8ec-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df8ec-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df8ec-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="df8ec-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df8ec-106">La méthode **obtenir \_ MediaCollection** obtient un pointeur vers l’interface [**ITMediaCollection**](itmediacollection.md) pour la Conférence.</span><span class="sxs-lookup"><span data-stu-id="df8ec-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df8ec-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="df8ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df8ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8ec-109">*ppMediaCollection* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df8ec-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df8ec-110">Pointeur vers [**ITMediaCollection**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="df8ec-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8ec-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df8ec-111">Return value</span></span>

<span data-ttu-id="df8ec-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="df8ec-112">This method can return one of these values.</span></span>



| <span data-ttu-id="df8ec-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="df8ec-113">Value</span></span>                                                                                                                           | <span data-ttu-id="df8ec-114">Signification</span><span class="sxs-lookup"><span data-stu-id="df8ec-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df8ec-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="df8ec-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="df8ec-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="df8ec-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="df8ec-118">Le paramètre *ppMediaCollection* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="df8ec-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="df8ec-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="df8ec-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="df8ec-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="df8ec-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="df8ec-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="df8ec-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="df8ec-123"><dt>**HRESULT \_ à partir du \_ code d’erreur \_ (erreur de \_ données non valides \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="df8ec-124">Une erreur interne s’est produite, généralement en raison de l’échec d’une méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="df8ec-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="df8ec-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="df8ec-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="df8ec-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="df8ec-127">Notes</span><span class="sxs-lookup"><span data-stu-id="df8ec-127">Remarks</span></span>

<span data-ttu-id="df8ec-128">Un pointeur [**ITMediaCollection**](itmediacollection.md) peut également être obtenu à l’aide de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="df8ec-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="df8ec-129">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMediaCollection**](itmediacollection.md) retournée par **ITSdp :: \_ MediaCollection**.</span><span class="sxs-lookup"><span data-stu-id="df8ec-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="df8ec-130">L’application doit appeler **Release** sur l’interface **ITMediaCollection** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="df8ec-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8ec-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df8ec-131">Requirements</span></span>



| <span data-ttu-id="df8ec-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df8ec-132">Requirement</span></span> | <span data-ttu-id="df8ec-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="df8ec-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df8ec-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="df8ec-134">TAPI version</span></span><br/> | <span data-ttu-id="df8ec-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df8ec-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df8ec-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="df8ec-136">Header</span></span><br/>       | <dl> <span data-ttu-id="df8ec-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="df8ec-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df8ec-138">Library</span></span><br/>      | <dl> <span data-ttu-id="df8ec-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df8ec-140">DLL</span><span class="sxs-lookup"><span data-stu-id="df8ec-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="df8ec-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df8ec-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8ec-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df8ec-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8ec-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="df8ec-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="df8ec-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="df8ec-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 





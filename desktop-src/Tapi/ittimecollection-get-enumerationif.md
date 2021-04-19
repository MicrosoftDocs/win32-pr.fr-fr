---
description: La méthode d’extraction \_ EnumerationIf retourne l’interface d’énumération IEnumTime qui énumère ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'ITTimeCollection :: get_EnumerationIf, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525425"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="bb6b6-103">ITTimeCollection :: \_ EnumerationIf, méthode</span><span class="sxs-lookup"><span data-stu-id="bb6b6-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="bb6b6-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb6b6-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bb6b6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bb6b6-106">La méthode d' **extraction \_ EnumerationIf** retourne l’interface d’énumération [**IEnumTime**](ienumtime.md) qui énumère [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="bb6b6-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb6b6-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bb6b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb6b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6b6-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bb6b6-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6b6-110">Pointeur vers l’interface [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="bb6b6-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6b6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb6b6-111">Return value</span></span>

<span data-ttu-id="bb6b6-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bb6b6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb6b6-113">Value</span></span>                                                                                         | <span data-ttu-id="bb6b6-114">Signification</span><span class="sxs-lookup"><span data-stu-id="bb6b6-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bb6b6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bb6b6-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bb6b6-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bb6b6-118">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="bb6b6-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bb6b6-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bb6b6-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bb6b6-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bb6b6-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bb6b6-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="bb6b6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="bb6b6-125">Remarks</span></span>

<span data-ttu-id="bb6b6-126">Cette méthode est interchangeable avec l’opération d’extraction de la valeur [**\_ \_ NewEnum**](ittimecollection-get--newenum.md) , sauf qu’elle retourne [**IEnumTime**](ienumtime.md) au lieu de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="bb6b6-127">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumTime**](ienumtime.md) retournée par **ITTimeCollection :: \_ EnumerationIf**.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="bb6b6-128">L’application doit appeler **Release** sur l’interface [**IEnumTime**](ienumtime.md) pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6b6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb6b6-129">Requirements</span></span>



| <span data-ttu-id="bb6b6-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb6b6-130">Requirement</span></span> | <span data-ttu-id="bb6b6-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb6b6-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6b6-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bb6b6-132">TAPI version</span></span><br/> | <span data-ttu-id="bb6b6-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb6b6-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bb6b6-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb6b6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="bb6b6-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb6b6-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb6b6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="bb6b6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bb6b6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bb6b6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="bb6b6-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6b6-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6b6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb6b6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6b6-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="bb6b6-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="bb6b6-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="bb6b6-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="bb6b6-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="bb6b6-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 





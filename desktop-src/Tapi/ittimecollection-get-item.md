---
description: La \_ méthode d’extraction d’élément obtient un élément de la collection à l’aide d’un index.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'ITTimeCollection :: get_Item, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520864"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="47179-103">ITTimeCollection :: obten, \_ méthode d’élément</span><span class="sxs-lookup"><span data-stu-id="47179-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="47179-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="47179-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47179-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="47179-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="47179-106">La méthode d' **extraction d' \_ élément** obtient un élément de la collection à l’aide d’un index.</span><span class="sxs-lookup"><span data-stu-id="47179-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="47179-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47179-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="47179-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47179-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47179-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47179-110">Index de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="47179-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="47179-111">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="47179-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47179-112">Pointeur vers [**ITTime**](ittime.md) interface souhaitée.</span><span class="sxs-lookup"><span data-stu-id="47179-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47179-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47179-113">Return value</span></span>

<span data-ttu-id="47179-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="47179-114">This method can return one of these values.</span></span>



| <span data-ttu-id="47179-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47179-115">Value</span></span>                                                                                         | <span data-ttu-id="47179-116">Signification</span><span class="sxs-lookup"><span data-stu-id="47179-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="47179-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47179-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="47179-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="47179-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="47179-120">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="47179-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="47179-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="47179-122">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="47179-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="47179-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="47179-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="47179-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="47179-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="47179-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="47179-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="47179-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="47179-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="47179-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="47179-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="47179-129">Notes</span><span class="sxs-lookup"><span data-stu-id="47179-129">Remarks</span></span>

<span data-ttu-id="47179-130">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTime**](ittime.md) retournée par I **TTimeCollection :: obten \_ Item**.</span><span class="sxs-lookup"><span data-stu-id="47179-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="47179-131">L’application doit appeler **Release** sur l’interface **ITTime** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="47179-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="47179-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47179-132">Requirements</span></span>



| <span data-ttu-id="47179-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47179-133">Requirement</span></span> | <span data-ttu-id="47179-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="47179-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47179-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="47179-135">TAPI version</span></span><br/> | <span data-ttu-id="47179-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="47179-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="47179-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="47179-137">Header</span></span><br/>       | <dl> <span data-ttu-id="47179-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="47179-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="47179-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47179-139">Library</span></span><br/>      | <dl> <span data-ttu-id="47179-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47179-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="47179-141">DLL</span><span class="sxs-lookup"><span data-stu-id="47179-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="47179-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47179-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47179-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47179-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47179-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="47179-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="47179-145">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="47179-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 





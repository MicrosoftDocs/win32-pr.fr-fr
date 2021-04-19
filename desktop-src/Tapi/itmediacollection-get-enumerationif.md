---
description: La \_ méthode obtenir EnumerationIf obtient un pointeur vers une interface d’énumération de média.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'ITMediaCollection :: get_EnumerationIf, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537991"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="7c9cd-103">ITMediaCollection :: \_ EnumerationIf, méthode</span><span class="sxs-lookup"><span data-stu-id="7c9cd-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="7c9cd-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c9cd-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7c9cd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7c9cd-106">La méthode **obtenir \_ EnumerationIf** obtient un pointeur vers une interface d’énumération de média.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c9cd-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7c9cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c9cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9cd-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7c9cd-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c9cd-110">Pointeur vers l’interface [**IEnumMedia**](ienummedia.md) pour l’élément souhaité.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9cd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c9cd-111">Return value</span></span>

<span data-ttu-id="7c9cd-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7c9cd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c9cd-113">Value</span></span>                                                                                         | <span data-ttu-id="7c9cd-114">Signification</span><span class="sxs-lookup"><span data-stu-id="7c9cd-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7c9cd-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7c9cd-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7c9cd-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7c9cd-118">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="7c9cd-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7c9cd-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7c9cd-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7c9cd-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7c9cd-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7c9cd-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7c9cd-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7c9cd-125">Remarks</span></span>

<span data-ttu-id="7c9cd-126">Cette méthode est interchangeable avec l’opération d’extraction de la valeur [**\_ \_ NewEnum**](itmediacollection-get--newenum.md) , sauf qu’elle retourne [**IEnumMedia**](ienummedia.md) au lieu de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="7c9cd-127">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumMedia**](ienummedia.md) retournée par **ITMediaCollection :: \_ Enumerationlf**.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="7c9cd-128">L’application doit appeler **Release** sur l’interface **IEnumMedia** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="7c9cd-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9cd-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c9cd-129">Requirements</span></span>



| <span data-ttu-id="7c9cd-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c9cd-130">Requirement</span></span> | <span data-ttu-id="7c9cd-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c9cd-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9cd-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7c9cd-132">TAPI version</span></span><br/> | <span data-ttu-id="7c9cd-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7c9cd-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7c9cd-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c9cd-134">Header</span></span><br/>       | <dl> <span data-ttu-id="7c9cd-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c9cd-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c9cd-136">Library</span></span><br/>      | <dl> <span data-ttu-id="7c9cd-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7c9cd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7c9cd-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="7c9cd-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c9cd-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9cd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c9cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9cd-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="7c9cd-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="7c9cd-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="7c9cd-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 





---
description: 'ITTimeCollection :: get__NewEnum méthode-la \_ \_ méthode obtenir NewEnum retourne un énumérateur pour la collection.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'ITTimeCollection :: get__NewEnum, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfc9d616efb58c6173f2c9c6e5913d27776958c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088887"
---
# <a name="ittimecollectionget__newenum-method"></a><span data-ttu-id="414ec-103">ITTimeCollection :: obtient la \_ \_ méthode NewEnum</span><span class="sxs-lookup"><span data-stu-id="414ec-103">ITTimeCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="414ec-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="414ec-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="414ec-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="414ec-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="414ec-106">La méthode **obtenir \_ \_ NewEnum** retourne un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="414ec-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="414ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="414ec-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="414ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="414ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="414ec-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="414ec-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="414ec-110">Pointeur vers une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur un objet énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="414ec-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="414ec-111">Appelez la méthode [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface **IUnknown** retournée pour obtenir un pointeur vers une interface d’énumération [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur la collection.</span><span class="sxs-lookup"><span data-stu-id="414ec-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="414ec-112">**IEnumVARIANT** fournit un certain nombre de méthodes que vous pouvez utiliser pour itérer au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="414ec-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="414ec-113">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="414ec-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="414ec-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="414ec-114">Return value</span></span>

<span data-ttu-id="414ec-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="414ec-115">This method can return one of these values.</span></span>



| <span data-ttu-id="414ec-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="414ec-116">Return code</span></span>                                                                                   | <span data-ttu-id="414ec-117">Description</span><span class="sxs-lookup"><span data-stu-id="414ec-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="414ec-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="414ec-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="414ec-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="414ec-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="414ec-121">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="414ec-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="414ec-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="414ec-123">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="414ec-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="414ec-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="414ec-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="414ec-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="414ec-126"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="414ec-127">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="414ec-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="414ec-128">Notes </span><span class="sxs-lookup"><span data-stu-id="414ec-128">Remarks</span></span>

<span data-ttu-id="414ec-129">Cette méthode est interchangeable avec la méthode [**\_ EnumerationIf**](ittimecollection-get-enumerationif.md) , sauf qu’elle retourne **IUnknown** au lieu de [**IEnumTime**](ienumtime.md).</span><span class="sxs-lookup"><span data-stu-id="414ec-129">This method is interchangeable with [**get\_EnumerationIf**](ittimecollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumTime**](ienumtime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="414ec-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414ec-130">Requirements</span></span>



| <span data-ttu-id="414ec-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="414ec-131">Requirement</span></span> | <span data-ttu-id="414ec-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="414ec-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="414ec-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="414ec-133">TAPI version</span></span><br/> | <span data-ttu-id="414ec-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="414ec-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="414ec-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="414ec-135">Header</span></span><br/>       | <dl> <span data-ttu-id="414ec-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="414ec-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="414ec-137">Library</span></span><br/>      | <dl> <span data-ttu-id="414ec-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="414ec-139">DLL</span><span class="sxs-lookup"><span data-stu-id="414ec-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="414ec-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="414ec-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414ec-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414ec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414ec-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="414ec-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="414ec-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="414ec-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 


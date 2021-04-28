---
description: 'ITMediaCollection :: get__NewEnum méthode-la \_ \_ méthode obtenir NewEnum retourne un énumérateur pour la collection.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'ITMediaCollection :: get__NewEnum, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098357"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="e9c5c-103">ITMediaCollection :: obtient la \_ \_ méthode NewEnum</span><span class="sxs-lookup"><span data-stu-id="e9c5c-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="e9c5c-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9c5c-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e9c5c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9c5c-106">La méthode **obtenir \_ \_ NewEnum** retourne un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c5c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9c5c-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e9c5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9c5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c5c-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9c5c-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c5c-110">Pointeur vers une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur un objet énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="e9c5c-111">Appelez la méthode [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface **IUnknown** retournée pour obtenir un pointeur vers une interface d’énumération [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur la collection.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="e9c5c-112">**IEnumVARIANT** fournit un certain nombre de méthodes que vous pouvez utiliser pour itérer au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="e9c5c-113">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c5c-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e9c5c-114">Return value</span></span>

<span data-ttu-id="e9c5c-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e9c5c-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e9c5c-116">Return code</span></span>                                                                                   | <span data-ttu-id="e9c5c-117">Description</span><span class="sxs-lookup"><span data-stu-id="e9c5c-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e9c5c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9c5c-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e9c5c-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e9c5c-121">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="e9c5c-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9c5c-123">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e9c5c-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e9c5c-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e9c5c-126"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e9c5c-127">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="e9c5c-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e9c5c-128">Notes </span><span class="sxs-lookup"><span data-stu-id="e9c5c-128">Remarks</span></span>

<span data-ttu-id="e9c5c-129">Cette méthode est interchangeable avec la méthode [**\_ EnumerationIf**](itmediacollection-get-enumerationif.md) , sauf qu’elle retourne **IUnknown** au lieu de [**IEnumMedia**](ienummedia.md).</span><span class="sxs-lookup"><span data-stu-id="e9c5c-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c5c-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9c5c-130">Requirements</span></span>



| <span data-ttu-id="e9c5c-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9c5c-131">Requirement</span></span> | <span data-ttu-id="e9c5c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9c5c-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c5c-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e9c5c-133">TAPI version</span></span><br/> | <span data-ttu-id="e9c5c-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e9c5c-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e9c5c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9c5c-135">Header</span></span><br/>       | <dl> <span data-ttu-id="e9c5c-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9c5c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9c5c-137">Library</span></span><br/>      | <dl> <span data-ttu-id="e9c5c-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e9c5c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c5c-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="e9c5c-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5c-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c5c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c5c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c5c-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="e9c5c-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 


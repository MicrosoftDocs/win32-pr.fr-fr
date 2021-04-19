---
description: La \_ méthode d’extraction d’élément obtient un pointeur ITMedia correspondant à l’index spécifié.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'ITMediaCollection :: get_Item, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521628"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="cc1c2-103">ITMediaCollection :: obten, \_ méthode d’élément</span><span class="sxs-lookup"><span data-stu-id="cc1c2-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="cc1c2-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc1c2-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cc1c2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cc1c2-106">La méthode d' **extraction d' \_ élément** obtient un pointeur [**ITMedia**](itmedia.md) correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc1c2-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cc1c2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc1c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1c2-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc1c2-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1c2-110">Index de l’élément multimédia à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="cc1c2-111">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc1c2-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1c2-112">Pointeur vers l’interface [**ITMedia**](itmedia.md) pour l’élément souhaité.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1c2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc1c2-113">Return value</span></span>

<span data-ttu-id="cc1c2-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cc1c2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc1c2-115">Value</span></span>                                                                                         | <span data-ttu-id="cc1c2-116">Signification</span><span class="sxs-lookup"><span data-stu-id="cc1c2-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cc1c2-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cc1c2-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cc1c2-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cc1c2-120">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="cc1c2-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cc1c2-122">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="cc1c2-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc1c2-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cc1c2-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cc1c2-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cc1c2-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cc1c2-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cc1c2-129">Notes</span><span class="sxs-lookup"><span data-stu-id="cc1c2-129">Remarks</span></span>

<span data-ttu-id="cc1c2-130">La plupart des listes C et C++ sont de base 0, mais cet index est basé sur 1 pour la compatibilité Visual Basic, ce qui signifie que le premier élément a un numéro d’index de 1.</span><span class="sxs-lookup"><span data-stu-id="cc1c2-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1c2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc1c2-131">Requirements</span></span>



| <span data-ttu-id="cc1c2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc1c2-132">Requirement</span></span> | <span data-ttu-id="cc1c2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc1c2-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1c2-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="cc1c2-134">TAPI version</span></span><br/> | <span data-ttu-id="cc1c2-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cc1c2-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cc1c2-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc1c2-136">Header</span></span><br/>       | <dl> <span data-ttu-id="cc1c2-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc1c2-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc1c2-138">Library</span></span><br/>      | <dl> <span data-ttu-id="cc1c2-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc1c2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cc1c2-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="cc1c2-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c2-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc1c2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc1c2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1c2-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="cc1c2-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="cc1c2-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="cc1c2-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 





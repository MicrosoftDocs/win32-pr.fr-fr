---
description: La méthode Create crée un nouveau média avec les propriétés par défaut, l’ajoute à la collection à l’index spécifié et retourne un pointeur vers l’interface ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection :: Create, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533230"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="e0dec-103">ITMediaCollection :: Create, méthode</span><span class="sxs-lookup"><span data-stu-id="e0dec-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="e0dec-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e0dec-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0dec-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e0dec-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0dec-106">La méthode **Create** crée un nouveau média avec les propriétés par défaut, l’ajoute à la collection à l’index spécifié et retourne un pointeur vers l’interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dec-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0dec-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="e0dec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0dec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0dec-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e0dec-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dec-110">Index du nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="e0dec-110">Index for the new item.</span></span> <span data-ttu-id="e0dec-111">La valeur minimale pour l’index est 1, et la valeur maximale pour l’index est le nombre actuel d’éléments + 1.</span><span class="sxs-lookup"><span data-stu-id="e0dec-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="e0dec-112">*ppMedia* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e0dec-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dec-113">Pointeur vers l’interface [**ITMedia**](itmedia.md) créée.</span><span class="sxs-lookup"><span data-stu-id="e0dec-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0dec-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0dec-114">Return value</span></span>

<span data-ttu-id="e0dec-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e0dec-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e0dec-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0dec-116">Value</span></span>                                                                                         | <span data-ttu-id="e0dec-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e0dec-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e0dec-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0dec-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="e0dec-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e0dec-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0dec-121">Le paramètre *ppMedia* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="e0dec-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="e0dec-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e0dec-123">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e0dec-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="e0dec-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0dec-125">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e0dec-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e0dec-126"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e0dec-127">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e0dec-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e0dec-128"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e0dec-129">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="e0dec-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e0dec-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e0dec-130">Remarks</span></span>

<span data-ttu-id="e0dec-131">La plupart des listes C et C++ sont de base 0, mais cet index est basé sur 1 pour la compatibilité Visual Basic, ce qui signifie que le premier élément a un numéro d’index de 1.</span><span class="sxs-lookup"><span data-stu-id="e0dec-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="e0dec-132">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMedia**](itmedia.md) retournée par **ITMediaCollection :: Create**.</span><span class="sxs-lookup"><span data-stu-id="e0dec-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="e0dec-133">L’application doit appeler **Release** sur l’interface [**ITMedia**](itmedia.md) pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="e0dec-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dec-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0dec-134">Requirements</span></span>



| <span data-ttu-id="e0dec-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0dec-135">Requirement</span></span> | <span data-ttu-id="e0dec-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0dec-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dec-137">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e0dec-137">TAPI version</span></span><br/> | <span data-ttu-id="e0dec-138">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e0dec-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e0dec-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0dec-139">Header</span></span><br/>       | <dl> <span data-ttu-id="e0dec-140"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0dec-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e0dec-141">Library</span></span><br/>      | <dl> <span data-ttu-id="e0dec-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e0dec-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e0dec-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0dec-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0dec-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0dec-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0dec-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dec-146">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="e0dec-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="e0dec-147">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="e0dec-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 





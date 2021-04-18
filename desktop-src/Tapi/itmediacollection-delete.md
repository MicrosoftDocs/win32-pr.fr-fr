---
description: La méthode Delete supprime le support correspondant à l’index spécifié.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ITMediaCollection ::D méthode supprimable (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526550"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="47143-103">ITMediaCollection ::D méthode supprimable</span><span class="sxs-lookup"><span data-stu-id="47143-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="47143-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="47143-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47143-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="47143-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="47143-106">La méthode **Delete** supprime le support correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="47143-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="47143-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47143-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="47143-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47143-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47143-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47143-110">Index du média à supprimer.</span><span class="sxs-lookup"><span data-stu-id="47143-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47143-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47143-111">Return value</span></span>

<span data-ttu-id="47143-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="47143-112">This method can return one of these values.</span></span>



| <span data-ttu-id="47143-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="47143-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="47143-114">Description</span><span class="sxs-lookup"><span data-stu-id="47143-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47143-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="47143-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="47143-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="47143-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="47143-118">Le paramètre d' *index* a une valeur inférieure à 1 ou supérieure au nombre actuel d’éléments.</span><span class="sxs-lookup"><span data-stu-id="47143-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="47143-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="47143-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="47143-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="47143-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="47143-122">Erreur interne (ne doit se produire que si un appel précédent a retourné une erreur).</span><span class="sxs-lookup"><span data-stu-id="47143-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="47143-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="47143-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="47143-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="47143-125"><dt>**HRESULT \_ à partir du \_ code d’erreur \_ (SDPBLB \_ conf \_ BLOB \_ détruit)**</dt></span><span class="sxs-lookup"><span data-stu-id="47143-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="47143-126">L’objet BLOB SDP n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="47143-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="47143-127">Notes</span><span class="sxs-lookup"><span data-stu-id="47143-127">Remarks</span></span>

<span data-ttu-id="47143-128">La plupart des listes C et C++ sont de base 0, mais cet index est basé sur 1 pour la compatibilité Visual Basic, ce qui signifie que le premier élément a un numéro d’index de 1.</span><span class="sxs-lookup"><span data-stu-id="47143-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="47143-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47143-129">Requirements</span></span>



| <span data-ttu-id="47143-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47143-130">Requirement</span></span> | <span data-ttu-id="47143-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="47143-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47143-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="47143-132">TAPI version</span></span><br/> | <span data-ttu-id="47143-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="47143-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="47143-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="47143-134">Header</span></span><br/>       | <dl> <span data-ttu-id="47143-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="47143-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="47143-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47143-136">Library</span></span><br/>      | <dl> <span data-ttu-id="47143-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47143-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="47143-138">DLL</span><span class="sxs-lookup"><span data-stu-id="47143-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="47143-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47143-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47143-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47143-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47143-141">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="47143-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 





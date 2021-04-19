---
title: Méthode IWMDRMDevice2 GetPartialSyncList
description: La méthode GetPartialSyncList obtient une liste de synchronisation partielle.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Méthode GetPartialSyncList Gestionnaire de périphériques Windows Media
- Méthode GetPartialSyncList Gestionnaire de périphériques Windows Media, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gestionnaire de périphériques, méthode GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541711"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="d4249-106">IWMDRMDevice2 :: GetPartialSyncList, méthode</span><span class="sxs-lookup"><span data-stu-id="d4249-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="d4249-107">La méthode **GetPartialSyncList** obtient une liste de synchronisation partielle.</span><span class="sxs-lookup"><span data-stu-id="d4249-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4249-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4249-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="d4249-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4249-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4249-110">*cMinCountThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4249-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-111">Seuil de nombre minimal.</span><span class="sxs-lookup"><span data-stu-id="d4249-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-112">*cMinHoursThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4249-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-113">Seuil d’heures minimum.</span><span class="sxs-lookup"><span data-stu-id="d4249-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-114">*dwStartingIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4249-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-115">Position de départ pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="d4249-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-116">*CItems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4249-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-117">Nombre d’éléments à indexer.</span><span class="sxs-lookup"><span data-stu-id="d4249-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-118">*ppbSyncList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4249-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-119">Liste de synchronisation de la licence récupérée.</span><span class="sxs-lookup"><span data-stu-id="d4249-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-120">*pcbSyncList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4249-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-121">Taille de la liste de synchronisation de licence, en octets.</span><span class="sxs-lookup"><span data-stu-id="d4249-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-122">*pdwNextStartingIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4249-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-123">Position de début suivante pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="d4249-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="d4249-124">*pcItemsProcessed* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4249-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4249-125">Nombre d’éléments en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="d4249-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4249-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4249-126">Return value</span></span>

<span data-ttu-id="d4249-127">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d4249-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4249-128">Toutes les méthodes d’interface dans Windows Media Gestionnaire de périphériques peuvent retourner l’une des classes de codes d’erreur suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4249-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="d4249-129">Codes d’erreur COM standard</span><span class="sxs-lookup"><span data-stu-id="d4249-129">Standard COM error codes</span></span>
-   <span data-ttu-id="d4249-130">Codes d’erreur Windows convertis en valeurs HRESULT</span><span class="sxs-lookup"><span data-stu-id="d4249-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="d4249-131">Codes d’erreur de Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="d4249-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="d4249-132">Pour obtenir une liste complète des codes d’erreur possibles, consultez [codes d’erreur](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4249-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4249-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4249-133">Requirements</span></span>



| <span data-ttu-id="d4249-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4249-134">Requirement</span></span> | <span data-ttu-id="d4249-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4249-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4249-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4249-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d4249-137"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4249-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4249-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4249-138">Library</span></span><br/> | <dl> <span data-ttu-id="d4249-139"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4249-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4249-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4249-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4249-141">**IWMDRMDevice::GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="d4249-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="d4249-142">**Interface IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="d4249-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 






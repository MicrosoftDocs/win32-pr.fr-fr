---
description: La méthode Delete supprime un composant ITTime.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: ITTimeCollection ::D méthode supprimable (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544081"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="8586e-103">ITTimeCollection ::D méthode supprimable</span><span class="sxs-lookup"><span data-stu-id="8586e-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="8586e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8586e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8586e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8586e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8586e-106">La méthode **Delete** supprime un composant [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="8586e-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8586e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8586e-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="8586e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8586e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8586e-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8586e-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8586e-110">Index du composant [**ITTime**](ittime.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8586e-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="8586e-111">(Le tableau d’index est de base un.)</span><span class="sxs-lookup"><span data-stu-id="8586e-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8586e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8586e-112">Return value</span></span>

<span data-ttu-id="8586e-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8586e-113">This method can return one of these values.</span></span>



| <span data-ttu-id="8586e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8586e-114">Value</span></span>                                                                                         | <span data-ttu-id="8586e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="8586e-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8586e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8586e-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8586e-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8586e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8586e-119">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8586e-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="8586e-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8586e-121">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8586e-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8586e-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8586e-123">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8586e-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8586e-124"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8586e-125">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="8586e-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8586e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8586e-126">Requirements</span></span>



| <span data-ttu-id="8586e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8586e-127">Requirement</span></span> | <span data-ttu-id="8586e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8586e-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8586e-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8586e-129">TAPI version</span></span><br/> | <span data-ttu-id="8586e-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8586e-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8586e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="8586e-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8586e-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8586e-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8586e-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8586e-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8586e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8586e-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8586e-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8586e-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8586e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8586e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8586e-138">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="8586e-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="8586e-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="8586e-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 





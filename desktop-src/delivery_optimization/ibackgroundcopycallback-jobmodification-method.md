---
title: Méthode IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: L’optimisation de la remise (DO) appelle votre implémentation de la méthode JobModification lorsque le travail a été modifié.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Méthode JobModification
- Méthode JobModification, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512383"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="d3a85-106">IBackgroundCopyCallback :: JobModification, méthode</span><span class="sxs-lookup"><span data-stu-id="d3a85-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="d3a85-107">L’optimisation de la remise (DO) appelle votre implémentation de la méthode [**JobModification**](https://www.bing.com/search?q=**JobModification**) lorsque le travail a été modifié.</span><span class="sxs-lookup"><span data-stu-id="d3a85-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="d3a85-108">Le service génère cet événement lorsque les octets sont transférés, que des fichiers ont été ajoutés au travail, que des propriétés ont été modifiées ou que l’état de la tâche a changé.</span><span class="sxs-lookup"><span data-stu-id="d3a85-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a85-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3a85-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="d3a85-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3a85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a85-111">*pJob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3a85-112">Contient les méthodes permettant d’accéder à la propriété, à la progression et aux informations d’État du travail.</span><span class="sxs-lookup"><span data-stu-id="d3a85-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="d3a85-113">Ne libérez pas *pJob*; Libère l’interface lorsque la méthode [**JOBMODIFICATION**](https://www.bing.com/search?q=**JobModification**) est retournée.</span><span class="sxs-lookup"><span data-stu-id="d3a85-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="d3a85-114">*dwReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3a85-115">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d3a85-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a85-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3a85-116">Return value</span></span>

<span data-ttu-id="d3a85-117">Cette méthode doit retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="d3a85-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a85-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3a85-118">Requirements</span></span>



| <span data-ttu-id="d3a85-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3a85-119">Requirement</span></span> | <span data-ttu-id="d3a85-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3a85-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a85-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3a85-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a85-122">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d3a85-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3a85-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a85-124">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3a85-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d3a85-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3a85-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a85-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3a85-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="d3a85-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3a85-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d3a85-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3a85-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3a85-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d3a85-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a85-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a85-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3a85-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d3a85-133">IID</span><span class="sxs-lookup"><span data-stu-id="d3a85-133">IID</span></span><br/>                      | <span data-ttu-id="d3a85-134">IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="d3a85-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d3a85-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3a85-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a85-136">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="d3a85-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="d3a85-137">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d3a85-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 






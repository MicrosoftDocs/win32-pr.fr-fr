---
title: Méthode IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: L’optimisation de la remise (DO) appelle votre implémentation de la méthode JobTransferred lorsque tous les fichiers du travail ont été transférés avec succès.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Méthode JobTransferred
- Méthode JobTransferred, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103513"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="3b140-106">IBackgroundCopyCallback :: JobTransferred, méthode</span><span class="sxs-lookup"><span data-stu-id="3b140-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="3b140-107">L’optimisation de la remise (DO) appelle votre implémentation de la méthode **JobTransferred** lorsque tous les fichiers du travail ont été transférés avec succès.</span><span class="sxs-lookup"><span data-stu-id="3b140-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b140-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b140-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="3b140-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b140-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b140-110">*pJob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b140-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b140-111">Contient des informations relatives au travail, telles que l’heure de fin du travail, le nombre d’octets transférés et le nombre de fichiers transférés.</span><span class="sxs-lookup"><span data-stu-id="3b140-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="3b140-112">Ne libérez pas *pJob*; Libère l’interface lorsque la méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="3b140-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b140-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b140-113">Return value</span></span>

<span data-ttu-id="3b140-114">Cette méthode doit retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="3b140-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b140-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3b140-115">Remarks</span></span>

<span data-ttu-id="3b140-116">En règle générale, votre implémentation doit appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour confirmer que les fichiers ont été transférés avec succès.</span><span class="sxs-lookup"><span data-stu-id="3b140-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="3b140-117">Les fichiers téléchargés et le fichier de réponse ne sont pas disponibles sur le client tant que vous n’avez pas appelé la méthode **Complete** .</span><span class="sxs-lookup"><span data-stu-id="3b140-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="3b140-118">Si vous n’appelez pas la méthode [**Complete**](ibackgroundcopyjob-complete.md) ou si la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) annule le travail au bout de 30 jours et supprime les fichiers incomplets.</span><span class="sxs-lookup"><span data-stu-id="3b140-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b140-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b140-119">Requirements</span></span>



| <span data-ttu-id="3b140-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b140-120">Requirement</span></span> | <span data-ttu-id="3b140-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b140-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b140-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b140-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b140-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b140-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3b140-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b140-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b140-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b140-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3b140-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b140-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b140-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b140-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b140-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b140-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b140-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b140-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b140-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b140-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b140-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b140-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3b140-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3b140-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b140-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b140-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3b140-134">IID</span><span class="sxs-lookup"><span data-stu-id="3b140-134">IID</span></span><br/>                      | <span data-ttu-id="3b140-135">IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="3b140-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3b140-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b140-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b140-137">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="3b140-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="3b140-138">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3b140-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3b140-139">**Méthode ibackgroundcopyjob :: complet**</span><span class="sxs-lookup"><span data-stu-id="3b140-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="3b140-140">**Méthode ibackgroundcopyjob :: Cancel**</span><span class="sxs-lookup"><span data-stu-id="3b140-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 






---
title: Méthode ibackgroundcopyjob GetDisplayName, méthode (Deliveryoptimization. h)
description: Récupère le nom complet du travail. En général, vous utilisez le nom complet pour identifier la tâche dans une interface utilisateur.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (méthode)
- GetDisplayName, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, GetDisplayName, méthode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942608"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="4dfd5-107">Méthode ibackgroundcopyjob :: GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="4dfd5-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="4dfd5-108">Récupère le nom complet du travail.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="4dfd5-109">En général, vous utilisez le nom complet pour identifier la tâche dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dfd5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dfd5-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="4dfd5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dfd5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dfd5-112">*ppDisplayName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4dfd5-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dfd5-113">Chaîne terminée par le caractère null qui contient le nom complet qui identifie le travail.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="4dfd5-114">Plusieurs travaux peuvent avoir le même nom complet.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-114">More than one job can have the same display name.</span></span> <span data-ttu-id="4dfd5-115">Appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer *ppDisplayName* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dfd5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4dfd5-116">Return value</span></span>

<span data-ttu-id="4dfd5-117">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="4dfd5-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4dfd5-118">Return code</span></span>                                                                                  | <span data-ttu-id="4dfd5-119">Description</span><span class="sxs-lookup"><span data-stu-id="4dfd5-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="4dfd5-120"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="4dfd5-121">Le nom d’affichage a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="4dfd5-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4dfd5-123">Le paramètre *ppDisplayName* ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4dfd5-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4dfd5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dfd5-124">Requirements</span></span>



| <span data-ttu-id="4dfd5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dfd5-125">Requirement</span></span> | <span data-ttu-id="4dfd5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dfd5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dfd5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dfd5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4dfd5-128">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dfd5-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4dfd5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dfd5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4dfd5-130">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dfd5-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4dfd5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dfd5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dfd5-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4dfd5-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="4dfd5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4dfd5-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4dfd5-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4dfd5-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dfd5-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4dfd5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4dfd5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dfd5-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dfd5-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4dfd5-139">IID</span><span class="sxs-lookup"><span data-stu-id="4dfd5-139">IID</span></span><br/>                      | <span data-ttu-id="4dfd5-140">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="4dfd5-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4dfd5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dfd5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dfd5-142">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="4dfd5-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 


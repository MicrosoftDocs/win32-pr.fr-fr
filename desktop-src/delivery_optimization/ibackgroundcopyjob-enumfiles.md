---
title: Méthode ibackgroundcopyjob EnumFiles, méthode (Deliveryoptimization. h)
description: Récupère un pointeur d’interface IEnumBackgroundCopyFiles que vous utilisez pour énumérer les fichiers dans un travail.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles, méthode
- EnumFiles, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104074"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="9db79-106">Méthode ibackgroundcopyjob :: EnumFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="9db79-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="9db79-107">Récupère un pointeur d’interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que vous utilisez pour énumérer les fichiers dans un travail.</span><span class="sxs-lookup"><span data-stu-id="9db79-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db79-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9db79-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="9db79-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9db79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db79-110">*ppEnumFiles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9db79-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db79-111">Pointeur d’interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que vous utilisez pour énumérer les fichiers du travail.</span><span class="sxs-lookup"><span data-stu-id="9db79-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="9db79-112">Libérez *ppEnumFiles* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="9db79-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db79-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9db79-113">Return value</span></span>

<span data-ttu-id="9db79-114">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9db79-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db79-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9db79-115">Requirements</span></span>



| <span data-ttu-id="9db79-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9db79-116">Requirement</span></span> | <span data-ttu-id="9db79-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9db79-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db79-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9db79-119">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9db79-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9db79-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db79-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9db79-121">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9db79-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9db79-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9db79-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db79-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db79-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9db79-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="9db79-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9db79-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9db79-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9db79-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9db79-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9db79-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9db79-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9db79-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9db79-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db79-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db79-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9db79-130">IID</span><span class="sxs-lookup"><span data-stu-id="9db79-130">IID</span></span><br/>                      | <span data-ttu-id="9db79-131">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="9db79-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9db79-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db79-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db79-133">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9db79-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9db79-134">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="9db79-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 






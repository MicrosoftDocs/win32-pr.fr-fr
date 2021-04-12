---
title: Méthode IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Récupère les plages que vous souhaitez télécharger à partir du fichier distant.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Méthode GetFileRanges
- Méthode GetFileRanges, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, méthode GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384512"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="3e5da-106">IBackgroundCopyFile2 :: GetFileRanges, méthode</span><span class="sxs-lookup"><span data-stu-id="3e5da-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="3e5da-107">Récupère les plages que vous souhaitez télécharger à partir du fichier distant.</span><span class="sxs-lookup"><span data-stu-id="3e5da-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e5da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e5da-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="3e5da-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e5da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e5da-110">*RangeCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e5da-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e5da-111">Nombre d’éléments dans les *plages*.</span><span class="sxs-lookup"><span data-stu-id="3e5da-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="3e5da-112">*Plages* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3e5da-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e5da-113">Tableau de structures de [**BG_FILE_RANGE**](bg-file-range.md) qui spécifient les plages à télécharger.</span><span class="sxs-lookup"><span data-stu-id="3e5da-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="3e5da-114">Lorsque vous avez terminé, appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer des *plages*.</span><span class="sxs-lookup"><span data-stu-id="3e5da-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e5da-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e5da-115">Return value</span></span>

<span data-ttu-id="3e5da-116">Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="3e5da-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="3e5da-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3e5da-117">Return code</span></span>                                                                              | <span data-ttu-id="3e5da-118">Description</span><span class="sxs-lookup"><span data-stu-id="3e5da-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e5da-119"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="3e5da-120">Succès</span><span class="sxs-lookup"><span data-stu-id="3e5da-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="3e5da-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="3e5da-122">Aucune plage n’a été spécifiée ou le travail est un travail de chargement ou de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="3e5da-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="3e5da-123">*RangeCount* a la valeur zéro et *Ranges* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="3e5da-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e5da-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e5da-124">Requirements</span></span>



| <span data-ttu-id="3e5da-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e5da-125">Requirement</span></span> | <span data-ttu-id="3e5da-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e5da-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5da-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e5da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3e5da-128">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e5da-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e5da-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e5da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3e5da-130">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e5da-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e5da-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e5da-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e5da-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e5da-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3e5da-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e5da-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e5da-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e5da-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e5da-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3e5da-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3e5da-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e5da-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e5da-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3e5da-139">IID</span><span class="sxs-lookup"><span data-stu-id="3e5da-139">IID</span></span><br/>                      | <span data-ttu-id="3e5da-140">IID_IBackgroundCopyFile2 est défini en tant que 83e81b93-0873-474d-8A8C-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="3e5da-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3e5da-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e5da-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e5da-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="3e5da-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="3e5da-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="3e5da-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 


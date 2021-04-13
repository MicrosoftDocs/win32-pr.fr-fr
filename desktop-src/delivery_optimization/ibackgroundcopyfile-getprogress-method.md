---
title: Méthode IBackgroundCopyFile GetProgress (Deliveryoptimization. h)
description: Récupère des informations sur la progression du transfert de fichiers.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Méthode GetProgress
- Méthode GetProgress, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, méthode GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465079"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="411dd-106">IBackgroundCopyFile :: GetProgress, méthode</span><span class="sxs-lookup"><span data-stu-id="411dd-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="411dd-107">Récupère des informations sur la progression du transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="411dd-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="411dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="411dd-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="411dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="411dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411dd-110">*pProgress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="411dd-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411dd-111">Structure dont les membres indiquent la progression du transfert de fichier.</span><span class="sxs-lookup"><span data-stu-id="411dd-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="411dd-112">Pour plus d’informations sur le type d’informations de progression disponibles, consultez la structure [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="411dd-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="411dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="411dd-113">Return value</span></span>

<span data-ttu-id="411dd-114">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="411dd-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="411dd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="411dd-115">Requirements</span></span>



| <span data-ttu-id="411dd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="411dd-116">Requirement</span></span> | <span data-ttu-id="411dd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="411dd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="411dd-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="411dd-119">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="411dd-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="411dd-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="411dd-121">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="411dd-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="411dd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="411dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="411dd-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="411dd-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="411dd-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="411dd-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="411dd-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="411dd-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="411dd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="411dd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="411dd-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="411dd-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="411dd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="411dd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411dd-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="411dd-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="411dd-130">IID</span><span class="sxs-lookup"><span data-stu-id="411dd-130">IID</span></span><br/>                      | <span data-ttu-id="411dd-131">IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="411dd-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="411dd-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="411dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411dd-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="411dd-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="411dd-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="411dd-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="411dd-135">**Méthode ibackgroundcopyjob :: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="411dd-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 






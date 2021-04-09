---
title: IEnumBackgroundCopyFiles GetCount, méthode (Deliveryoptimization. h)
description: Récupère le nombre de fichiers dans l’énumération.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (méthode)
- GetCount, méthode, IEnumBackgroundCopyFiles, interface
- Interface IEnumBackgroundCopyFiles, GetCount, méthode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741469"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="2eb97-106">IEnumBackgroundCopyFiles :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="2eb97-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="2eb97-107">Récupère le nombre de fichiers dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2eb97-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb97-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2eb97-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="2eb97-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2eb97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb97-110">*pCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2eb97-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb97-111">Nombre de fichiers dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2eb97-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb97-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2eb97-112">Return value</span></span>

<span data-ttu-id="2eb97-113">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2eb97-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb97-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2eb97-114">Requirements</span></span>



| <span data-ttu-id="2eb97-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2eb97-115">Requirement</span></span> | <span data-ttu-id="2eb97-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2eb97-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb97-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb97-118">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eb97-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2eb97-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb97-120">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eb97-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2eb97-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2eb97-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb97-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb97-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2eb97-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="2eb97-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2eb97-124"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2eb97-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2eb97-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2eb97-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2eb97-126"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eb97-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2eb97-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2eb97-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eb97-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eb97-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2eb97-129">IID</span><span class="sxs-lookup"><span data-stu-id="2eb97-129">IID</span></span><br/>                      | <span data-ttu-id="2eb97-130">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="2eb97-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="2eb97-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eb97-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb97-132">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="2eb97-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 






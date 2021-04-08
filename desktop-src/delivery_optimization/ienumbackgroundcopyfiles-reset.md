---
title: Méthode de réinitialisation IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Réinitialise la séquence d'énumération au début.
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset (méthode)
- Reset, méthode, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, méthode Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843385"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="061dd-106">IEnumBackgroundCopyFiles :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="061dd-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="061dd-107">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="061dd-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="061dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="061dd-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="061dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="061dd-109">Parameters</span></span>

<span data-ttu-id="061dd-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="061dd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="061dd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="061dd-111">Return value</span></span>

<span data-ttu-id="061dd-112">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="061dd-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="061dd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="061dd-113">Requirements</span></span>



| <span data-ttu-id="061dd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="061dd-114">Requirement</span></span> | <span data-ttu-id="061dd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="061dd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061dd-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="061dd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="061dd-117">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="061dd-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="061dd-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="061dd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="061dd-119">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="061dd-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="061dd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="061dd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="061dd-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="061dd-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="061dd-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="061dd-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="061dd-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="061dd-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="061dd-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="061dd-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="061dd-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="061dd-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="061dd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="061dd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061dd-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061dd-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="061dd-128">IID</span><span class="sxs-lookup"><span data-stu-id="061dd-128">IID</span></span><br/>                      | <span data-ttu-id="061dd-129">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="061dd-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="061dd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="061dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061dd-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="061dd-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 






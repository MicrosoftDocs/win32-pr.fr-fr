---
title: Méthode de réinitialisation IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: 'IEnumBackgroundCopyFiles :: Reset, méthode-réinitialise la séquence d’énumération au début.'
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
ms.openlocfilehash: d6800095d0a6f20ef8b632830a224d4da27356bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105487"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="7f34a-106">IEnumBackgroundCopyFiles :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="7f34a-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="7f34a-107">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="7f34a-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f34a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f34a-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="7f34a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f34a-109">Parameters</span></span>

<span data-ttu-id="7f34a-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f34a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f34a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f34a-111">Return value</span></span>

<span data-ttu-id="7f34a-112">Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f34a-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f34a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f34a-113">Requirements</span></span>



| <span data-ttu-id="7f34a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f34a-114">Requirement</span></span> | <span data-ttu-id="7f34a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f34a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f34a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f34a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f34a-117">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7f34a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f34a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f34a-119">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f34a-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f34a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f34a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f34a-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f34a-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="7f34a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f34a-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7f34a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f34a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f34a-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7f34a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7f34a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f34a-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f34a-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7f34a-128">IID</span><span class="sxs-lookup"><span data-stu-id="7f34a-128">IID</span></span><br/>                      | <span data-ttu-id="7f34a-129">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="7f34a-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7f34a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f34a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f34a-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="7f34a-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 






---
title: Interface IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Utilisez l’interface IEnumBackgroundCopyFiles pour énumérer les fichiers contenus dans un travail. Pour récupérer un pointeur d’interface IEnumBackgroundCopyFiles, appelez la méthode EnumFiles méthode ibackgroundcopyjob.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Description
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527569"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="46ffc-106">Interface IEnumBackgroundCopyFiles</span><span class="sxs-lookup"><span data-stu-id="46ffc-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="46ffc-107">Utilisez l’interface **IEnumBackgroundCopyFiles** pour énumérer les fichiers contenus dans un travail.</span><span class="sxs-lookup"><span data-stu-id="46ffc-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="46ffc-108">Pour récupérer un pointeur d’interface **IEnumBackgroundCopyFiles** , appelez la méthode [**méthode ibackgroundcopyjob :: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="46ffc-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="46ffc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="46ffc-109">Members</span></span>

<span data-ttu-id="46ffc-110">L’interface **IEnumBackgroundCopyFiles** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="46ffc-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46ffc-111">**IEnumBackgroundCopyFiles** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46ffc-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="46ffc-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46ffc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46ffc-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46ffc-113">Methods</span></span>

<span data-ttu-id="46ffc-114">L’interface **IEnumBackgroundCopyFiles** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="46ffc-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="46ffc-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="46ffc-115">Method</span></span>                                                | <span data-ttu-id="46ffc-116">Description</span><span class="sxs-lookup"><span data-stu-id="46ffc-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="46ffc-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="46ffc-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="46ffc-118">Récupère le nombre d’éléments dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="46ffc-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="46ffc-119">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="46ffc-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="46ffc-120">Récupère un nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="46ffc-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="46ffc-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="46ffc-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="46ffc-122">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="46ffc-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="46ffc-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="46ffc-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="46ffc-124">Ignore un nombre défini d'éléments dans la séquence d'énumération.</span><span class="sxs-lookup"><span data-stu-id="46ffc-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="46ffc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46ffc-125">Requirements</span></span>



| <span data-ttu-id="46ffc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46ffc-126">Requirement</span></span> | <span data-ttu-id="46ffc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ffc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ffc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ffc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46ffc-129">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ffc-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="46ffc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ffc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46ffc-131">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ffc-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="46ffc-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="46ffc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="46ffc-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ffc-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="46ffc-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="46ffc-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46ffc-135"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46ffc-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="46ffc-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46ffc-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="46ffc-137"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46ffc-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="46ffc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="46ffc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46ffc-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46ffc-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="46ffc-140">IID</span><span class="sxs-lookup"><span data-stu-id="46ffc-140">IID</span></span><br/>                      | <span data-ttu-id="46ffc-141">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="46ffc-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="46ffc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ffc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ffc-143">**Méthode ibackgroundcopyjob :: EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="46ffc-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 


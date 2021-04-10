---
title: Interface IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Utilisez cette interface pour récupérer ou définir les propriétés génériques des transferts de fichiers d’optimisation de la remise (DO).
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103505"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="cae36-105">Interface IBackgroundCopyFile5</span><span class="sxs-lookup"><span data-stu-id="cae36-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="cae36-106">Utilisez cette interface pour récupérer ou définir les propriétés génériques des transferts de fichiers d’optimisation de la remise (DO).</span><span class="sxs-lookup"><span data-stu-id="cae36-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="cae36-107">Pour obtenir un pointeur d’interface **IBackgroundCopyFile5** , appelez la méthode **IBackgroundCopyFile :: QueryInterface** à l’aide de __uuidof (IBackgroundCopyFile5) pour l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="cae36-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="cae36-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cae36-108">Members</span></span>

<span data-ttu-id="cae36-109">L’interface **IBackgroundCopyFile5** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cae36-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cae36-110">**IBackgroundCopyFile5** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cae36-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="cae36-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cae36-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cae36-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cae36-112">Methods</span></span>

<span data-ttu-id="cae36-113">L’interface **IBackgroundCopyFile5** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cae36-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="cae36-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="cae36-114">Method</span></span>                                                  | <span data-ttu-id="cae36-115">Description</span><span class="sxs-lookup"><span data-stu-id="cae36-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="cae36-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="cae36-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="cae36-117">Obtient la valeur d’une propriété BackgroundCopyFile générique.</span><span class="sxs-lookup"><span data-stu-id="cae36-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="cae36-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="cae36-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="cae36-119">Définit la valeur d’une propriété BackgroundCopyFile générique.</span><span class="sxs-lookup"><span data-stu-id="cae36-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cae36-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cae36-120">Requirements</span></span>



| <span data-ttu-id="cae36-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cae36-121">Requirement</span></span> | <span data-ttu-id="cae36-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cae36-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae36-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cae36-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cae36-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cae36-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cae36-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cae36-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cae36-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cae36-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cae36-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="cae36-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae36-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae36-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="cae36-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="cae36-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cae36-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cae36-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="cae36-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cae36-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="cae36-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae36-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="cae36-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cae36-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae36-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae36-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="cae36-135">IID</span><span class="sxs-lookup"><span data-stu-id="cae36-135">IID</span></span><br/>                      | <span data-ttu-id="cae36-136">IID_IBackgroundCopyFile5 est défini en tant que 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="cae36-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="cae36-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cae36-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae36-138">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="cae36-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="cae36-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="cae36-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 


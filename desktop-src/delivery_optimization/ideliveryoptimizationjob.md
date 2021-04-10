---
title: Interface IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Utilisez l’interface IDeliveryOptimizationJob pour télécharger des plages d’un fichier.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103654"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="9af66-105">Interface IDeliveryOptimizationJob</span><span class="sxs-lookup"><span data-stu-id="9af66-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="9af66-106">Utilisez l’interface **IDeliveryOptimizationJob** pour télécharger des plages d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9af66-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="9af66-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9af66-107">Members</span></span>

<span data-ttu-id="9af66-108">L’interface **IDeliveryOptimizationJob** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9af66-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9af66-109">**IDeliveryOptimizationJob** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9af66-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="9af66-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9af66-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9af66-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9af66-111">Methods</span></span>

<span data-ttu-id="9af66-112">L’interface **IDeliveryOptimizationJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9af66-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="9af66-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="9af66-113">Method</span></span>                                                                  | <span data-ttu-id="9af66-114">Description</span><span class="sxs-lookup"><span data-stu-id="9af66-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9af66-115">**AddFileWithRanges**</span><span class="sxs-lookup"><span data-stu-id="9af66-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="9af66-116">Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="9af66-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9af66-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9af66-117">Requirements</span></span>



| <span data-ttu-id="9af66-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9af66-118">Requirement</span></span> | <span data-ttu-id="9af66-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9af66-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af66-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af66-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9af66-121">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af66-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9af66-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af66-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9af66-123">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af66-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9af66-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9af66-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af66-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af66-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9af66-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="9af66-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9af66-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9af66-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9af66-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9af66-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="9af66-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9af66-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9af66-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9af66-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af66-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af66-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9af66-132">IID</span><span class="sxs-lookup"><span data-stu-id="9af66-132">IID</span></span><br/>                      | <span data-ttu-id="9af66-133">IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="9af66-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 


---
title: Interface IDeliveryOptimizationFile
description: Implémentez l’interface IDeliveryOptimizationFile pour identifier l’état d’un fichier spécifique.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509709"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="6f4d6-105">Interface IDeliveryOptimizationFile</span><span class="sxs-lookup"><span data-stu-id="6f4d6-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="6f4d6-106">Implémentez l’interface **IDeliveryOptimizationFile** pour identifier l’état d’un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="6f4d6-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="6f4d6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6f4d6-107">Members</span></span>

<span data-ttu-id="6f4d6-108">L’interface **IDeliveryOptimizationFile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f4d6-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f4d6-109">**IDeliveryOptimizationFile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f4d6-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="6f4d6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f4d6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f4d6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f4d6-111">Methods</span></span>

<span data-ttu-id="6f4d6-112">L’interface **IDeliveryOptimizationFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6f4d6-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="6f4d6-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f4d6-113">Method</span></span>                                                 | <span data-ttu-id="6f4d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="6f4d6-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="6f4d6-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="6f4d6-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="6f4d6-116">Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="6f4d6-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="6f4d6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f4d6-117">Requirements</span></span>

| <span data-ttu-id="6f4d6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f4d6-118">Requirement</span></span> | <span data-ttu-id="6f4d6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f4d6-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6f4d6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f4d6-120">Minimum supported client</span></span>      | <span data-ttu-id="6f4d6-121">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f4d6-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="6f4d6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f4d6-122">Minimum supported server</span></span>      | <span data-ttu-id="6f4d6-123">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f4d6-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="6f4d6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f4d6-124">Header</span></span>                        | <span data-ttu-id="6f4d6-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="6f4d6-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="6f4d6-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="6f4d6-126">IDL</span></span>                           | <span data-ttu-id="6f4d6-127">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="6f4d6-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="6f4d6-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f4d6-128">Library</span></span>                       | <span data-ttu-id="6f4d6-129">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="6f4d6-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="6f4d6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4d6-130">DLL</span></span>                           | <span data-ttu-id="6f4d6-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="6f4d6-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="6f4d6-132">IID</span><span class="sxs-lookup"><span data-stu-id="6f4d6-132">IID</span></span>                           | <span data-ttu-id="6f4d6-133">IID_IDeliveryOptimizationFile est défini en tant que B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="6f4d6-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |

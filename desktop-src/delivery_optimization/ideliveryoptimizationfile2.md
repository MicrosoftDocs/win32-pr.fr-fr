---
title: Interface IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 prend en charge le paramétrage et l’obtention des propriétés de fichier facultatives.
keywords:
- Interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032629"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="38262-105">Interface IDeliveryOptimizationFile2</span><span class="sxs-lookup"><span data-stu-id="38262-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="38262-106">**IDeliveryOptimizationFile2** prend en charge le paramétrage et l’obtention des propriétés de fichier facultatives.</span><span class="sxs-lookup"><span data-stu-id="38262-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="38262-107">Membres</span><span class="sxs-lookup"><span data-stu-id="38262-107">Members</span></span>

<span data-ttu-id="38262-108">L’interface **IDeliveryOptimizationFile2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="38262-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="38262-109">**IDeliveryOptimizationFile2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="38262-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="38262-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="38262-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="38262-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="38262-111">Methods</span></span>

<span data-ttu-id="38262-112">L’interface **IDeliveryOptimizationFile2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="38262-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="38262-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="38262-113">Method</span></span>                                                 | <span data-ttu-id="38262-114">Description</span><span class="sxs-lookup"><span data-stu-id="38262-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="38262-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="38262-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="38262-116">Cette méthode retourne une seule propriété du fichier DO.</span><span class="sxs-lookup"><span data-stu-id="38262-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="38262-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="38262-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="38262-118">Cette méthode définit une seule propriété du fichier DO.</span><span class="sxs-lookup"><span data-stu-id="38262-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="38262-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38262-119">Requirements</span></span>

| <span data-ttu-id="38262-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38262-120">Requirement</span></span> | <span data-ttu-id="38262-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="38262-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="38262-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38262-122">Minimum supported client</span></span>      | <span data-ttu-id="38262-123">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38262-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="38262-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38262-124">Minimum supported server</span></span>      | <span data-ttu-id="38262-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38262-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="38262-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="38262-126">Header</span></span>                        | <span data-ttu-id="38262-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="38262-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="38262-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="38262-128">IDL</span></span>                           | <span data-ttu-id="38262-129">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="38262-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="38262-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38262-130">Library</span></span>                       | <span data-ttu-id="38262-131">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="38262-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="38262-132">DLL</span><span class="sxs-lookup"><span data-stu-id="38262-132">DLL</span></span>                           | <span data-ttu-id="38262-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="38262-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="38262-134">IID</span><span class="sxs-lookup"><span data-stu-id="38262-134">IID</span></span>                           | <span data-ttu-id="38262-135">IID_IDeliveryOptimizationFile2 est défini en tant que 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="38262-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |

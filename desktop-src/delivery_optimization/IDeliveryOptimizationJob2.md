---
title: Interface IDeliveryOptimizationJob2
description: 'En savoir plus sur : interface IDeliveryOptimizationJob2'
keywords:
- Interface IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519220"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="f6183-104">Interface IDeliveryOptimizationJob2</span><span class="sxs-lookup"><span data-stu-id="f6183-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="f6183-105">Le IDeliveryOptimizationJob2 permet d’ajouter un seul fichier au travail de téléchargement et de récupérer le fichier immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f6183-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="f6183-106">Cette interface prend également en charge la définition et l’obtention des propriétés de travaux facultatives.</span><span class="sxs-lookup"><span data-stu-id="f6183-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="f6183-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f6183-107">Members</span></span>

<span data-ttu-id="f6183-108">L’interface **IDeliveryOptimizationJob2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f6183-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f6183-109">**IDeliveryOptimizationJob2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f6183-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="f6183-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f6183-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f6183-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f6183-111">Methods</span></span>

<span data-ttu-id="f6183-112">L’interface **IDeliveryOptimizationJob2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f6183-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="f6183-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f6183-113">Method</span></span>                                              | <span data-ttu-id="f6183-114">Description</span><span class="sxs-lookup"><span data-stu-id="f6183-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="f6183-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="f6183-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="f6183-116">La méthode AddFile ajoute un seul fichier à une tâche DO existante.</span><span class="sxs-lookup"><span data-stu-id="f6183-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="f6183-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="f6183-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="f6183-118">La méthode AddFile ajoute un seul fichier à une tâche DO existante.</span><span class="sxs-lookup"><span data-stu-id="f6183-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="f6183-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="f6183-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="f6183-120">Cette méthode n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f6183-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="f6183-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6183-121">Requirements</span></span>

| <span data-ttu-id="f6183-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6183-122">Requirement</span></span> | <span data-ttu-id="f6183-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6183-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6183-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6183-124">Minimum supported client</span></span> | <span data-ttu-id="f6183-125">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6183-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="f6183-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6183-126">Minimum supported server</span></span> | <span data-ttu-id="f6183-127">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6183-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="f6183-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6183-128">Header</span></span>                   | <span data-ttu-id="f6183-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="f6183-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="f6183-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="f6183-130">IDL</span></span>                      | <span data-ttu-id="f6183-131">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="f6183-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="f6183-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6183-132">Library</span></span>                  | <span data-ttu-id="f6183-133">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="f6183-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="f6183-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f6183-134">DLL</span></span>                      | <span data-ttu-id="f6183-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="f6183-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="f6183-136">IID</span><span class="sxs-lookup"><span data-stu-id="f6183-136">IID</span></span>                      | <span data-ttu-id="f6183-137">IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="f6183-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

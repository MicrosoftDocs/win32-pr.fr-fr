---
title: IDeliveryOptimizationFile GetStats, méthode (Deliveryoptimization. h)
description: Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (méthode)
- GetStats, méthode, interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, GetStats, méthode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385088"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="03305-106">IDeliveryOptimizationFile :: GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="03305-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="03305-107">Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="03305-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="03305-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03305-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="03305-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03305-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03305-110">*swarmStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03305-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03305-111">Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="03305-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="03305-112">Pour plus d’informations, consultez la structure [**DOSwarmStats**](doswarmstats.md) .</span><span class="sxs-lookup"><span data-stu-id="03305-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03305-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03305-113">Return value</span></span>

<span data-ttu-id="03305-114">Cette méthode doit retourner **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="03305-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="03305-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03305-115">Requirements</span></span>



| <span data-ttu-id="03305-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03305-116">Requirement</span></span> | <span data-ttu-id="03305-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="03305-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03305-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03305-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03305-119">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03305-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03305-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03305-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03305-121">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03305-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="03305-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="03305-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03305-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="03305-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="03305-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="03305-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03305-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03305-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="03305-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03305-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="03305-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03305-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="03305-128">DLL</span><span class="sxs-lookup"><span data-stu-id="03305-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03305-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03305-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="03305-130">IID</span><span class="sxs-lookup"><span data-stu-id="03305-130">IID</span></span><br/>                      | <span data-ttu-id="03305-131">IID_IDeliveryOptimizationFile est défini en tant que B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="03305-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="03305-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03305-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03305-133">**IDeliveryOptimizationFile**</span><span class="sxs-lookup"><span data-stu-id="03305-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 






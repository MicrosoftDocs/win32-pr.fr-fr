---
title: Identificateurs de poids de filtre (Fwpmu. h)
description: Identificateurs de poids de filtre utilisés par le moteur de filtrage de base (BFE) pour calculer les pondérations de filtre générées automatiquement.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513629"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="4a2e7-103">Identificateurs de poids de filtre</span><span class="sxs-lookup"><span data-stu-id="4a2e7-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="4a2e7-104">Les identificateurs de poids de filtre utilisés par le moteur de filtrage de base (BFE) pour calculer les pondérations de filtre générées automatiquement sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="4a2e7-105">Pour plus d’informations sur la génération de poids de filtre, consultez [assignation de poids de filtre](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2e7-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="4a2e7-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bits de \_ poids \_ automatique FWPM**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2e7-107">(60)</span><span class="sxs-lookup"><span data-stu-id="4a2e7-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="4a2e7-108">Nombre de bits utilisés pour les pondérations de filtre générées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2e7-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ - \_ poids automatique \_ maximal**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2e7-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="4a2e7-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="4a2e7-111">Poids maximal du filtre généré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2e7-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2e7-113">0XC</span><span class="sxs-lookup"><span data-stu-id="4a2e7-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="4a2e7-114">BFE affecte un poids avec cette valeur de plage aux filtres IKE et AuthIP.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="4a2e7-115">Pour plus d’informations sur les filtres IKE/AuthIP, consultez [exemptions IKE/AuthIP](ike-exemptions.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2e7-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2e7-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_plage de poids FWPM \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2e7-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="4a2e7-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="4a2e7-118">BFE affecte un poids avec cette valeur de plage aux filtres de stratégie IPsec.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2e7-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM \_ de \_ poids \_ maximal**</span><span class="sxs-lookup"><span data-stu-id="4a2e7-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2e7-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="4a2e7-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="4a2e7-121">Valeur maximale de la plage de poids du filtre autorisée.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="4a2e7-122">**MAXUINT64** représente la plus grande valeur possible de **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="4a2e7-123">La valeur de cette constante est 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4a2e7-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a2e7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a2e7-124">Requirements</span></span>



| <span data-ttu-id="4a2e7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a2e7-125">Requirement</span></span> | <span data-ttu-id="4a2e7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a2e7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2e7-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a2e7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2e7-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a2e7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a2e7-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a2e7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2e7-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a2e7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a2e7-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a2e7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2e7-132"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e7-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






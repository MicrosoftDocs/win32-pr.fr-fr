---
title: Constantes DirectML
description: Les constantes suivantes sont déclarées dans `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539858"
---
# <a name="directml-constants"></a><span data-ttu-id="d4e67-104">Constantes DirectML</span><span class="sxs-lookup"><span data-stu-id="d4e67-104">DirectML constants</span></span>

<span data-ttu-id="d4e67-105">Les constantes suivantes sont déclarées dans `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="d4e67-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="d4e67-106">Constante</span><span class="sxs-lookup"><span data-stu-id="d4e67-106">Constant</span></span> | <span data-ttu-id="d4e67-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e67-107">Value</span></span> | <span data-ttu-id="d4e67-108">Description</span><span class="sxs-lookup"><span data-stu-id="d4e67-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="d4e67-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="d4e67-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="d4e67-110">5</span><span class="sxs-lookup"><span data-stu-id="d4e67-110">5</span></span> | <span data-ttu-id="d4e67-111">Les dizaines de DirectML prennent en charge un maximum de 5 dimensions pour DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="d4e67-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="d4e67-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="d4e67-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="d4e67-113">8</span><span class="sxs-lookup"><span data-stu-id="d4e67-113">8</span></span> | <span data-ttu-id="d4e67-114">Les dizaines de DirectML prennent en charge un maximum de 8 Dimensions pour DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="d4e67-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="d4e67-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="d4e67-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="d4e67-116">256</span><span class="sxs-lookup"><span data-stu-id="d4e67-116">256</span></span> | <span data-ttu-id="d4e67-117">Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets.</span><span class="sxs-lookup"><span data-stu-id="d4e67-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="d4e67-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="d4e67-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="d4e67-119">256</span><span class="sxs-lookup"><span data-stu-id="d4e67-119">256</span></span> | <span data-ttu-id="d4e67-120">Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets.</span><span class="sxs-lookup"><span data-stu-id="d4e67-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="d4e67-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="d4e67-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="d4e67-122">16</span><span class="sxs-lookup"><span data-stu-id="d4e67-122">16</span></span> | <span data-ttu-id="d4e67-123">Les dizaines de tampons ont une exigence d’alignement d’adresse de base minimale de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="d4e67-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d4e67-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4e67-124">Requirements</span></span>

| <span data-ttu-id="d4e67-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4e67-125">Requirement</span></span> | <span data-ttu-id="d4e67-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4e67-126">Value</span></span> |
|-|-|
| <span data-ttu-id="d4e67-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4e67-127">Header</span></span> | <span data-ttu-id="d4e67-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="d4e67-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="d4e67-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4e67-129">See also</span></span>

* [<span data-ttu-id="d4e67-130">Référence DirectML</span><span class="sxs-lookup"><span data-stu-id="d4e67-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="d4e67-131">Référence de base</span><span class="sxs-lookup"><span data-stu-id="d4e67-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="d4e67-132">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d4e67-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)

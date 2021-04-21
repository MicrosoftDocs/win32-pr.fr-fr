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
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803410"
---
# <a name="directml-constants"></a><span data-ttu-id="60b81-104">Constantes DirectML</span><span class="sxs-lookup"><span data-stu-id="60b81-104">DirectML constants</span></span>

<span data-ttu-id="60b81-105">Les constantes suivantes sont déclarées dans `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="60b81-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="60b81-106">Constante</span><span class="sxs-lookup"><span data-stu-id="60b81-106">Constant</span></span> | <span data-ttu-id="60b81-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b81-107">Value</span></span> | <span data-ttu-id="60b81-108">Description</span><span class="sxs-lookup"><span data-stu-id="60b81-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="60b81-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="60b81-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="60b81-110">5</span><span class="sxs-lookup"><span data-stu-id="60b81-110">5</span></span> | <span data-ttu-id="60b81-111">Les dizaines de DirectML prennent en charge un maximum de 5 dimensions pour DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="60b81-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="60b81-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="60b81-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="60b81-113">8</span><span class="sxs-lookup"><span data-stu-id="60b81-113">8</span></span> | <span data-ttu-id="60b81-114">Les dizaines de DirectML prennent en charge un maximum de 8 Dimensions pour DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="60b81-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="60b81-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="60b81-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="60b81-116">256</span><span class="sxs-lookup"><span data-stu-id="60b81-116">256</span></span> | <span data-ttu-id="60b81-117">Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets.</span><span class="sxs-lookup"><span data-stu-id="60b81-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="60b81-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="60b81-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="60b81-119">256</span><span class="sxs-lookup"><span data-stu-id="60b81-119">256</span></span> | <span data-ttu-id="60b81-120">Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets.</span><span class="sxs-lookup"><span data-stu-id="60b81-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="60b81-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="60b81-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="60b81-122">16</span><span class="sxs-lookup"><span data-stu-id="60b81-122">16</span></span> | <span data-ttu-id="60b81-123">Les dizaines de tampons ont une exigence d’alignement d’adresse de base minimale de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="60b81-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="60b81-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="60b81-124">Requirements</span></span>

| <span data-ttu-id="60b81-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b81-125">Requirement</span></span> | <span data-ttu-id="60b81-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b81-126">Value</span></span> |
|-|-|
| <span data-ttu-id="60b81-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="60b81-127">Header</span></span> | <span data-ttu-id="60b81-128">DirectML. h</span><span class="sxs-lookup"><span data-stu-id="60b81-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="60b81-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b81-129">See also</span></span>

* [<span data-ttu-id="60b81-130">Référence DirectML</span><span class="sxs-lookup"><span data-stu-id="60b81-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="60b81-131">Référence de base</span><span class="sxs-lookup"><span data-stu-id="60b81-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="60b81-132">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="60b81-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)

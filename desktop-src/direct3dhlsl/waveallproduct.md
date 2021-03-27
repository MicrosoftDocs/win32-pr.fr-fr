---
title: WaveActiveProduct fonction)
description: Multiplie les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- WaveActiveProduct fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842885"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="17239-104">WaveActiveProduct fonction)</span><span class="sxs-lookup"><span data-stu-id="17239-104">WaveActiveProduct function</span></span>

<span data-ttu-id="17239-105">Multiplie les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="17239-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="17239-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17239-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="17239-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17239-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17239-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="17239-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="17239-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="17239-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17239-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17239-110">Return value</span></span>

<span data-ttu-id="17239-111">Valeur du produit.</span><span class="sxs-lookup"><span data-stu-id="17239-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17239-112">Notes</span><span class="sxs-lookup"><span data-stu-id="17239-112">Remarks</span></span>

<span data-ttu-id="17239-113">L’ordre des opérations n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="17239-113">The order of operations is undefined.</span></span>

<span data-ttu-id="17239-114">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17239-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="17239-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17239-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17239-116">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="17239-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="17239-117">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="17239-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





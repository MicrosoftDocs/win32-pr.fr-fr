---
title: QuadReadLaneAt fonction)
description: Retourne la valeur source spécifiée à partir du Lane identifié par l’ID Lane dans le quad actuel.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463926"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="8e6a0-104">QuadReadLaneAt fonction)</span><span class="sxs-lookup"><span data-stu-id="8e6a0-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="8e6a0-105">Retourne la valeur source spécifiée à partir du Lane identifié par l’ID Lane dans le quad actuel.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e6a0-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="8e6a0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e6a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e6a0-108">*sourceValue*</span><span class="sxs-lookup"><span data-stu-id="8e6a0-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="8e6a0-109">Type demandé.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="8e6a0-110">*quadLaneID*</span><span class="sxs-lookup"><span data-stu-id="8e6a0-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="8e6a0-111">ID Lane ; Il s’agit d’une valeur comprise entre 0 et 3.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e6a0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e6a0-112">Return value</span></span>

<span data-ttu-id="8e6a0-113">Valeur source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-113">The specified source value.</span></span> <span data-ttu-id="8e6a0-114">Le résultat de cette fonction est uniforme sur le quadruple.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="8e6a0-115">Si le couloir source est inactif, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e6a0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8e6a0-116">Remarks</span></span>

<span data-ttu-id="8e6a0-117">Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="8e6a0-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="8e6a0-118">Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.</span><span class="sxs-lookup"><span data-stu-id="8e6a0-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="8e6a0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e6a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e6a0-120">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="8e6a0-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





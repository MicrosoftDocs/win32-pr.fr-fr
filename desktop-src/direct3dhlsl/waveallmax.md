---
title: WaveActiveMax fonction)
description: Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104383384"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="511fa-104">WaveActiveMax fonction)</span><span class="sxs-lookup"><span data-stu-id="511fa-104">WaveActiveMax function</span></span>

<span data-ttu-id="511fa-105">Retourne la valeur maximale de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="511fa-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="511fa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="511fa-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="511fa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="511fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511fa-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="511fa-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="511fa-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="511fa-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511fa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="511fa-110">Return value</span></span>

<span data-ttu-id="511fa-111">Valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="511fa-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="511fa-112">Notes</span><span class="sxs-lookup"><span data-stu-id="511fa-112">Remarks</span></span>

<span data-ttu-id="511fa-113">L’ordre des opérations n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="511fa-113">The order of operations is undefined.</span></span>

<span data-ttu-id="511fa-114">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="511fa-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="511fa-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="511fa-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="511fa-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="511fa-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511fa-117">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="511fa-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="511fa-118">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="511fa-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: WaveActiveBallot fonction)
description: Retourne un uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508197"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="a262f-104">WaveActiveBallot fonction)</span><span class="sxs-lookup"><span data-stu-id="a262f-104">WaveActiveBallot function</span></span>

<span data-ttu-id="a262f-105">Retourne un uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="a262f-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="a262f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a262f-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="a262f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a262f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a262f-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="a262f-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="a262f-109">Expression booléenne à évaluer.</span><span class="sxs-lookup"><span data-stu-id="a262f-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a262f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a262f-110">Return value</span></span>

<span data-ttu-id="a262f-111">Uint4 contenant un masque de masque de l’évaluation de l’expression booléenne pour tous les couloirs actifs dans l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="a262f-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="a262f-112">Le bit le moins significatif correspond à la voie avec l’index zéro.</span><span class="sxs-lookup"><span data-stu-id="a262f-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="a262f-113">Les bits correspondant aux couloirs inactifs sont nuls.</span><span class="sxs-lookup"><span data-stu-id="a262f-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="a262f-114">Les bits qui sont supérieurs ou égaux à [**WaveGetLaneCount**](wavegetlanecount.md) seront nuls.</span><span class="sxs-lookup"><span data-stu-id="a262f-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a262f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a262f-115">Remarks</span></span>

<span data-ttu-id="a262f-116">Les différents GPU ont des largeurs de processeur SIMD différentes (nombre de voies Lane).</span><span class="sxs-lookup"><span data-stu-id="a262f-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="a262f-117">La plupart de ces fonctions **WaveXXX** peuvent fonctionner au niveau d’abstraction où la largeur de l’ordinateur SIMD est masquée.</span><span class="sxs-lookup"><span data-stu-id="a262f-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="a262f-118">Pour optimiser la portabilité du code sur les GPU, utilisez les fonctions intrinsèques qui ne reposent pas sur la largeur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a262f-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="a262f-119">Par exemple, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a262f-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="a262f-120">À la place de :</span><span class="sxs-lookup"><span data-stu-id="a262f-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="a262f-121">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a262f-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="a262f-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="a262f-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="a262f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a262f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a262f-124">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="a262f-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a262f-125">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="a262f-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





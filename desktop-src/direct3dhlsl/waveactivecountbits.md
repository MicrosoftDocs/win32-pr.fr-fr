---
title: WaveActiveCountBits fonction)
description: Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104316866"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="2a27b-104">WaveActiveCountBits fonction)</span><span class="sxs-lookup"><span data-stu-id="2a27b-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="2a27b-105">Compte le nombre de variables booléennes qui ont la valeur true sur tous les couloirs actifs de l’onde actuelle, et réplique le résultat sur tous les couloirs de l’onde.</span><span class="sxs-lookup"><span data-stu-id="2a27b-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a27b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a27b-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="2a27b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a27b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a27b-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="2a27b-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="2a27b-109">Variables booléennes à évaluer.</span><span class="sxs-lookup"><span data-stu-id="2a27b-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="2a27b-110">La fourniture d’une valeur booléenne True explicite retourne le nombre de couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="2a27b-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a27b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a27b-111">Return value</span></span>

<span data-ttu-id="2a27b-112">Nombre dont la valeur est true sur tous les couloirs actifs de l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a27b-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a27b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2a27b-113">Remarks</span></span>

<span data-ttu-id="2a27b-114">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2a27b-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="2a27b-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="2a27b-115">Examples</span></span>

<span data-ttu-id="2a27b-116">Cela peut être implémenté plus efficacement qu’un WaveActiveSum complet, comme décrit dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="2a27b-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="2a27b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a27b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a27b-118">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="2a27b-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2a27b-119">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="2a27b-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





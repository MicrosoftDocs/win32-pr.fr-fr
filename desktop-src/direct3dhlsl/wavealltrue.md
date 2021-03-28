---
title: WaveActiveAllTrue fonction)
description: Retourne la valeur true si l’expression est vraie dans tous les couloirs actifs de l’onde actuelle.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- WaveActiveAllTrue fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463922"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="76d99-104">WaveActiveAllTrue fonction)</span><span class="sxs-lookup"><span data-stu-id="76d99-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="76d99-105">Retourne la valeur true si l’expression est vraie dans tous les couloirs actifs de l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="76d99-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d99-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76d99-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="76d99-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76d99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d99-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="76d99-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="76d99-109">Expression booléenne à évaluer.</span><span class="sxs-lookup"><span data-stu-id="76d99-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d99-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76d99-110">Return value</span></span>

<span data-ttu-id="76d99-111">True si l’expression est vraie dans tous les couloirs.</span><span class="sxs-lookup"><span data-stu-id="76d99-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d99-112">Notes</span><span class="sxs-lookup"><span data-stu-id="76d99-112">Remarks</span></span>

<span data-ttu-id="76d99-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="76d99-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="76d99-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76d99-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d99-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="76d99-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="76d99-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="76d99-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





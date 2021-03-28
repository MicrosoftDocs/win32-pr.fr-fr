---
title: WaveActiveAnyTrue fonction)
description: Retourne la valeur true si l’expression est vraie dans l’un des couloirs actifs de l’onde actuelle.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991029"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="a54a9-104">WaveActiveAnyTrue fonction)</span><span class="sxs-lookup"><span data-stu-id="a54a9-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="a54a9-105">Retourne la valeur true si l’expression est vraie dans l’un des couloirs actifs de l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="a54a9-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54a9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a54a9-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="a54a9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a54a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54a9-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="a54a9-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="a54a9-109">Expression booléenne à évaluer.</span><span class="sxs-lookup"><span data-stu-id="a54a9-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54a9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a54a9-110">Return value</span></span>

<span data-ttu-id="a54a9-111">True si l’expression est vraie dans une voie.</span><span class="sxs-lookup"><span data-stu-id="a54a9-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="a54a9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a54a9-112">Remarks</span></span>

<span data-ttu-id="a54a9-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a54a9-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="a54a9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a54a9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54a9-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="a54a9-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a54a9-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="a54a9-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





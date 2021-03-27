---
title: WaveActiveAllEqual fonction)
description: Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734797"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="19867-104">WaveActiveAllEqual fonction)</span><span class="sxs-lookup"><span data-stu-id="19867-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="19867-105">Retourne la valeur true si l’expression est la même pour chaque voie active de l’onde actuelle (et donc uniforme sur celle-ci).</span><span class="sxs-lookup"><span data-stu-id="19867-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="19867-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19867-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="19867-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19867-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19867-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="19867-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="19867-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="19867-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19867-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19867-110">Return value</span></span>

<span data-ttu-id="19867-111">True si l’expression est la même pour chaque voie active de l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="19867-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="19867-112">Notes</span><span class="sxs-lookup"><span data-stu-id="19867-112">Remarks</span></span>

<span data-ttu-id="19867-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="19867-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="19867-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19867-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19867-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="19867-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="19867-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="19867-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





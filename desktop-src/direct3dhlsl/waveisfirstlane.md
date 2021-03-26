---
title: WaveIsFirstLane fonction)
description: Retourne true uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane fonction HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316776"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="f3e7b-104">WaveIsFirstLane fonction)</span><span class="sxs-lookup"><span data-stu-id="f3e7b-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="f3e7b-105">Retourne true uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.</span><span class="sxs-lookup"><span data-stu-id="f3e7b-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3e7b-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="f3e7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3e7b-107">Parameters</span></span>

<span data-ttu-id="f3e7b-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3e7b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3e7b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3e7b-109">Return value</span></span>

<span data-ttu-id="f3e7b-110">True uniquement pour la voie active dans l’onde actuelle avec l’index le plus petit.</span><span class="sxs-lookup"><span data-stu-id="f3e7b-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e7b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3e7b-111">Remarks</span></span>

<span data-ttu-id="f3e7b-112">Cette fonction peut être utilisée pour identifier les opérations qui doivent être exécutées une seule fois par vague.</span><span class="sxs-lookup"><span data-stu-id="f3e7b-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="f3e7b-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f3e7b-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="f3e7b-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="f3e7b-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="f3e7b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e7b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e7b-116">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="f3e7b-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="f3e7b-117">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="f3e7b-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





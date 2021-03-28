---
title: WaveGetLaneCount fonction)
description: Retourne le nombre de couloirs dans une vague sur cette architecture.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount fonction HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383284"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="a8ec2-104">WaveGetLaneCount fonction)</span><span class="sxs-lookup"><span data-stu-id="a8ec2-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="a8ec2-105">Retourne le nombre de couloirs dans une vague sur cette architecture.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ec2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8ec2-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="a8ec2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8ec2-107">Parameters</span></span>

<span data-ttu-id="a8ec2-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8ec2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8ec2-109">Return value</span></span>

<span data-ttu-id="a8ec2-110">Le résultat sera compris entre 4 et 128, et comprend toutes les vagues : les pistes active, inactive et/ou d’assistance.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="a8ec2-111">Le résultat retourné par cette fonction peut varier considérablement en fonction de l’implémentation du pilote.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ec2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a8ec2-112">Remarks</span></span>

<span data-ttu-id="a8ec2-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="a8ec2-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8ec2-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="a8ec2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8ec2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ec2-116">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="a8ec2-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a8ec2-117">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="a8ec2-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





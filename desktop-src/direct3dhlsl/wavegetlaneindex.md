---
title: WaveGetLaneIndex fonction)
description: Retourne l’index de la voie active dans l’onde actuelle.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex fonction HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991032"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="7aa2d-104">WaveGetLaneIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="7aa2d-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="7aa2d-105">Retourne l’index de la voie active dans l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="7aa2d-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa2d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7aa2d-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="7aa2d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7aa2d-107">Parameters</span></span>

<span data-ttu-id="7aa2d-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7aa2d-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7aa2d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7aa2d-109">Return value</span></span>

<span data-ttu-id="7aa2d-110">Index Lane actuel.</span><span class="sxs-lookup"><span data-stu-id="7aa2d-110">The current lane index.</span></span> <span data-ttu-id="7aa2d-111">Le résultat sera compris entre 0 et le résultat renvoyé par [**WaveGetLaneCount**](wavegetlanecount.md).</span><span class="sxs-lookup"><span data-stu-id="7aa2d-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa2d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7aa2d-112">Remarks</span></span>

<span data-ttu-id="7aa2d-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="7aa2d-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="7aa2d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7aa2d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa2d-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="7aa2d-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7aa2d-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="7aa2d-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





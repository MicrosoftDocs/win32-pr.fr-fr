---
title: QuadReadAcrossX fonction)
description: Retourne la valeur locale spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102553"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="38ec0-104">QuadReadAcrossX fonction)</span><span class="sxs-lookup"><span data-stu-id="38ec0-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="38ec0-105">Retourne la valeur locale spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X.</span><span class="sxs-lookup"><span data-stu-id="38ec0-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ec0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38ec0-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="38ec0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38ec0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ec0-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="38ec0-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="38ec0-109">Type demandé.</span><span class="sxs-lookup"><span data-stu-id="38ec0-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ec0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38ec0-110">Return value</span></span>

<span data-ttu-id="38ec0-111">Valeur locale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="38ec0-111">The specified local value.</span></span> <span data-ttu-id="38ec0-112">Si le couloir source est inactif, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="38ec0-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ec0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="38ec0-113">Remarks</span></span>

<span data-ttu-id="38ec0-114">Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="38ec0-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="38ec0-115">Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.</span><span class="sxs-lookup"><span data-stu-id="38ec0-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="38ec0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38ec0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ec0-117">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="38ec0-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





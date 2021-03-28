---
title: QuadReadAcrossY fonction)
description: Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971811"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="297c3-104">QuadReadAcrossY fonction)</span><span class="sxs-lookup"><span data-stu-id="297c3-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="297c3-105">Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y.</span><span class="sxs-lookup"><span data-stu-id="297c3-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="297c3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="297c3-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="297c3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="297c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297c3-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="297c3-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="297c3-109">Type demandé.</span><span class="sxs-lookup"><span data-stu-id="297c3-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297c3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="297c3-110">Return value</span></span>

<span data-ttu-id="297c3-111">Valeur source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="297c3-111">The specified source value.</span></span> <span data-ttu-id="297c3-112">Si le couloir source est inactif, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="297c3-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="297c3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="297c3-113">Remarks</span></span>

<span data-ttu-id="297c3-114">Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="297c3-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="297c3-115">Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.</span><span class="sxs-lookup"><span data-stu-id="297c3-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="297c3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="297c3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297c3-117">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="297c3-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





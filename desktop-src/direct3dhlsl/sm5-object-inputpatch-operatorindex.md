---
title: 'InputPatch :: Operator, fonction'
description: 'Retourne le nième point de contrôle dans le correctif. | InputPatch :: Operator, fonction'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211466"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="72c82-105">InputPatch :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="72c82-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="72c82-106">Retourne le *n*<sup>ième</sup> point de contrôle dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="72c82-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c82-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72c82-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="72c82-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72c82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c82-109">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72c82-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c82-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="72c82-110">Type: **uint**</span></span>

<span data-ttu-id="72c82-111">Index d’entrée.</span><span class="sxs-lookup"><span data-stu-id="72c82-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c82-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72c82-112">Return value</span></span>

<span data-ttu-id="72c82-113">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="72c82-113">Type: **T**</span></span>

<span data-ttu-id="72c82-114">*N*<sup>ième</sup> point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="72c82-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c82-115">Notes</span><span class="sxs-lookup"><span data-stu-id="72c82-115">Remarks</span></span>

<span data-ttu-id="72c82-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="72c82-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="72c82-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="72c82-117">Vertex</span></span> | <span data-ttu-id="72c82-118">Forme</span><span class="sxs-lookup"><span data-stu-id="72c82-118">Hull</span></span> | <span data-ttu-id="72c82-119">Domain</span><span class="sxs-lookup"><span data-stu-id="72c82-119">Domain</span></span> | <span data-ttu-id="72c82-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="72c82-120">Geometry</span></span> | <span data-ttu-id="72c82-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="72c82-121">Pixel</span></span> | <span data-ttu-id="72c82-122">Compute</span><span class="sxs-lookup"><span data-stu-id="72c82-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="72c82-123">x</span><span class="sxs-lookup"><span data-stu-id="72c82-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="72c82-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72c82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c82-125">InputPatch</span><span class="sxs-lookup"><span data-stu-id="72c82-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="72c82-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="72c82-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





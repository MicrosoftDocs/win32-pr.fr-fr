---
title: 'OutputPatch :: Operator, fonction'
description: 'Retourne le nième point de contrôle dans le correctif. | OutputPatch :: Operator, fonction'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322061"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="7f8b0-105">OutputPatch :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="7f8b0-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="7f8b0-106">Retourne le *n*<sup>ième</sup> point de contrôle dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="7f8b0-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8b0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f8b0-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="7f8b0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f8b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8b0-109">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f8b0-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8b0-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7f8b0-110">Type: **uint**</span></span>

<span data-ttu-id="7f8b0-111">Index d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f8b0-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8b0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f8b0-112">Return value</span></span>

<span data-ttu-id="7f8b0-113">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="7f8b0-113">Type: **T**</span></span>

<span data-ttu-id="7f8b0-114">*N*<sup>ième</sup> point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7f8b0-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8b0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7f8b0-115">Remarks</span></span>

<span data-ttu-id="7f8b0-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="7f8b0-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7f8b0-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="7f8b0-117">Vertex</span></span> | <span data-ttu-id="7f8b0-118">Forme</span><span class="sxs-lookup"><span data-stu-id="7f8b0-118">Hull</span></span> | <span data-ttu-id="7f8b0-119">Domain</span><span class="sxs-lookup"><span data-stu-id="7f8b0-119">Domain</span></span> | <span data-ttu-id="7f8b0-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7f8b0-120">Geometry</span></span> | <span data-ttu-id="7f8b0-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="7f8b0-121">Pixel</span></span> | <span data-ttu-id="7f8b0-122">Compute</span><span class="sxs-lookup"><span data-stu-id="7f8b0-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7f8b0-123">x</span><span class="sxs-lookup"><span data-stu-id="7f8b0-123">x</span></span>    | <span data-ttu-id="7f8b0-124">x</span><span class="sxs-lookup"><span data-stu-id="7f8b0-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7f8b0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8b0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8b0-126">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="7f8b0-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="7f8b0-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7f8b0-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





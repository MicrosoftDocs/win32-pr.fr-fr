---
title: 'RWStructuredBuffer :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWStructuredBuffer :: Operator, fonction'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530633"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="1274f-105">RWStructuredBuffer :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="1274f-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="1274f-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="1274f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1274f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1274f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="1274f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1274f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1274f-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1274f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1274f-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1274f-110">Type: **uint**</span></span>

<span data-ttu-id="1274f-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="1274f-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1274f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1274f-112">Return value</span></span>

<span data-ttu-id="1274f-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="1274f-113">Type: **R**</span></span>

<span data-ttu-id="1274f-114">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="1274f-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1274f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1274f-115">Remarks</span></span>

<span data-ttu-id="1274f-116">Une ressource structurée peut être indexée en fonction des noms de composants des structures.</span><span class="sxs-lookup"><span data-stu-id="1274f-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="1274f-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1274f-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1274f-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="1274f-118">Vertex</span></span> | <span data-ttu-id="1274f-119">Forme</span><span class="sxs-lookup"><span data-stu-id="1274f-119">Hull</span></span> | <span data-ttu-id="1274f-120">Domain</span><span class="sxs-lookup"><span data-stu-id="1274f-120">Domain</span></span> | <span data-ttu-id="1274f-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1274f-121">Geometry</span></span> | <span data-ttu-id="1274f-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="1274f-122">Pixel</span></span> | <span data-ttu-id="1274f-123">Compute</span><span class="sxs-lookup"><span data-stu-id="1274f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1274f-124">x</span><span class="sxs-lookup"><span data-stu-id="1274f-124">x</span></span>     | <span data-ttu-id="1274f-125">x</span><span class="sxs-lookup"><span data-stu-id="1274f-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1274f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1274f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1274f-127">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="1274f-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1274f-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1274f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





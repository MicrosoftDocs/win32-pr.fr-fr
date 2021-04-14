---
title: 'RWBuffer :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWBuffer :: Operator, fonction'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991877"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="fda47-105">RWBuffer :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="fda47-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="fda47-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="fda47-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fda47-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="fda47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fda47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda47-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fda47-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda47-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="fda47-110">Type: **uint**</span></span>

<span data-ttu-id="fda47-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="fda47-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda47-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fda47-112">Return value</span></span>

<span data-ttu-id="fda47-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="fda47-113">Type: **R**</span></span>

<span data-ttu-id="fda47-114">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="fda47-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda47-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fda47-115">Remarks</span></span>

<span data-ttu-id="fda47-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fda47-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fda47-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="fda47-117">Vertex</span></span> | <span data-ttu-id="fda47-118">Forme</span><span class="sxs-lookup"><span data-stu-id="fda47-118">Hull</span></span> | <span data-ttu-id="fda47-119">Domain</span><span class="sxs-lookup"><span data-stu-id="fda47-119">Domain</span></span> | <span data-ttu-id="fda47-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="fda47-120">Geometry</span></span> | <span data-ttu-id="fda47-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="fda47-121">Pixel</span></span> | <span data-ttu-id="fda47-122">Compute</span><span class="sxs-lookup"><span data-stu-id="fda47-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fda47-123">x</span><span class="sxs-lookup"><span data-stu-id="fda47-123">x</span></span>      | <span data-ttu-id="fda47-124">x</span><span class="sxs-lookup"><span data-stu-id="fda47-124">x</span></span>    | <span data-ttu-id="fda47-125">x</span><span class="sxs-lookup"><span data-stu-id="fda47-125">x</span></span>      | <span data-ttu-id="fda47-126">x</span><span class="sxs-lookup"><span data-stu-id="fda47-126">x</span></span>        | <span data-ttu-id="fda47-127">x</span><span class="sxs-lookup"><span data-stu-id="fda47-127">x</span></span>     | <span data-ttu-id="fda47-128">x</span><span class="sxs-lookup"><span data-stu-id="fda47-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fda47-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fda47-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda47-130">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="fda47-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="fda47-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="fda47-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





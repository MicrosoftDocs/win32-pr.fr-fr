---
title: 'Texture1D :: Operator, fonction'
description: Retourne une variable de ressource en lecture seule pour un Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102716"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="3b096-104">Texture1D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="3b096-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="3b096-105">Retourne une variable de ressource en lecture seule pour un [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="3b096-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b096-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b096-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="3b096-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b096-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b096-108">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b096-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b096-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3b096-109">Type: **uint**</span></span>

<span data-ttu-id="3b096-110">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="3b096-110">The index position.</span></span> <span data-ttu-id="3b096-111">Contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="3b096-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b096-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b096-112">Return value</span></span>

<span data-ttu-id="3b096-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="3b096-113">Type: **R**</span></span>

<span data-ttu-id="3b096-114">Variable de ressource en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3b096-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b096-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3b096-115">Remarks</span></span>

<span data-ttu-id="3b096-116">Cette méthode accède toujours au premier niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="3b096-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="3b096-117">Pour spécifier d’autres niveaux MIP, utilisez plutôt l' [**opérateur \[ \] \[ \] MIP.**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="3b096-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="3b096-118">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3b096-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3b096-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="3b096-119">Vertex</span></span> | <span data-ttu-id="3b096-120">Forme</span><span class="sxs-lookup"><span data-stu-id="3b096-120">Hull</span></span> | <span data-ttu-id="3b096-121">Domain</span><span class="sxs-lookup"><span data-stu-id="3b096-121">Domain</span></span> | <span data-ttu-id="3b096-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3b096-122">Geometry</span></span> | <span data-ttu-id="3b096-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="3b096-123">Pixel</span></span> | <span data-ttu-id="3b096-124">Compute</span><span class="sxs-lookup"><span data-stu-id="3b096-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3b096-125">x</span><span class="sxs-lookup"><span data-stu-id="3b096-125">x</span></span>      | <span data-ttu-id="3b096-126">x</span><span class="sxs-lookup"><span data-stu-id="3b096-126">x</span></span>    | <span data-ttu-id="3b096-127">x</span><span class="sxs-lookup"><span data-stu-id="3b096-127">x</span></span>      | <span data-ttu-id="3b096-128">x</span><span class="sxs-lookup"><span data-stu-id="3b096-128">x</span></span>        | <span data-ttu-id="3b096-129">x</span><span class="sxs-lookup"><span data-stu-id="3b096-129">x</span></span>     | <span data-ttu-id="3b096-130">x</span><span class="sxs-lookup"><span data-stu-id="3b096-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3b096-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b096-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b096-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b096-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="3b096-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3b096-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





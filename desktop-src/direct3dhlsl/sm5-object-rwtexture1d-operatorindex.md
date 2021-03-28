---
title: 'RWTexture1D :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture1D :: Operator, fonction'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530615"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="60672-105">RWTexture1D :: Operator, fonction</span><span class="sxs-lookup"><span data-stu-id="60672-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="60672-106">Retourne une variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="60672-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="60672-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60672-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="60672-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60672-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60672-109">*pos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60672-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60672-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="60672-110">Type: **uint**</span></span>

<span data-ttu-id="60672-111">Position d’index.</span><span class="sxs-lookup"><span data-stu-id="60672-111">The index position.</span></span> <span data-ttu-id="60672-112">Contient la coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="60672-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60672-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60672-113">Return value</span></span>

<span data-ttu-id="60672-114">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="60672-114">Type: **R**</span></span>

<span data-ttu-id="60672-115">Variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="60672-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="60672-116">Notes</span><span class="sxs-lookup"><span data-stu-id="60672-116">Remarks</span></span>

<span data-ttu-id="60672-117">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="60672-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="60672-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="60672-118">Vertex</span></span> | <span data-ttu-id="60672-119">Forme</span><span class="sxs-lookup"><span data-stu-id="60672-119">Hull</span></span> | <span data-ttu-id="60672-120">Domain</span><span class="sxs-lookup"><span data-stu-id="60672-120">Domain</span></span> | <span data-ttu-id="60672-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="60672-121">Geometry</span></span> | <span data-ttu-id="60672-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="60672-122">Pixel</span></span> | <span data-ttu-id="60672-123">Compute</span><span class="sxs-lookup"><span data-stu-id="60672-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="60672-124">x</span><span class="sxs-lookup"><span data-stu-id="60672-124">x</span></span>     | <span data-ttu-id="60672-125">x</span><span class="sxs-lookup"><span data-stu-id="60672-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="60672-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60672-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60672-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="60672-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="60672-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="60672-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





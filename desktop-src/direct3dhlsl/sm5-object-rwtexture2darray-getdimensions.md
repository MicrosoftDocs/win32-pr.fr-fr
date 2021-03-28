---
title: 'RWTexture2DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture2DArray :: GetDimensions,, fonction'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211366"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="9e43b-105">RWTexture2DArray :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="9e43b-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="9e43b-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9e43b-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e43b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e43b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="9e43b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e43b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e43b-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e43b-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e43b-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e43b-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9e43b-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="9e43b-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="9e43b-112">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e43b-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e43b-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e43b-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9e43b-114">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="9e43b-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="9e43b-115">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e43b-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e43b-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e43b-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9e43b-117">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9e43b-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e43b-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9e43b-118">Return value</span></span>

<span data-ttu-id="9e43b-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9e43b-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e43b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9e43b-120">Remarks</span></span>

<span data-ttu-id="9e43b-121">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9e43b-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="9e43b-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9e43b-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9e43b-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="9e43b-123">Vertex</span></span> | <span data-ttu-id="9e43b-124">Forme</span><span class="sxs-lookup"><span data-stu-id="9e43b-124">Hull</span></span> | <span data-ttu-id="9e43b-125">Domain</span><span class="sxs-lookup"><span data-stu-id="9e43b-125">Domain</span></span> | <span data-ttu-id="9e43b-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9e43b-126">Geometry</span></span> | <span data-ttu-id="9e43b-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="9e43b-127">Pixel</span></span> | <span data-ttu-id="9e43b-128">Compute</span><span class="sxs-lookup"><span data-stu-id="9e43b-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9e43b-129">x</span><span class="sxs-lookup"><span data-stu-id="9e43b-129">x</span></span>     | <span data-ttu-id="9e43b-130">x</span><span class="sxs-lookup"><span data-stu-id="9e43b-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9e43b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e43b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e43b-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="9e43b-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="9e43b-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9e43b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

---
title: 'Texture2DMSArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DMSArray :: GetDimensions,, fonction'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322465"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="b6716-105">Texture2DMSArray :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="b6716-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="b6716-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b6716-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6716-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6716-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="b6716-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6716-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6716-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6716-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6716-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6716-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6716-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="b6716-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="b6716-112">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6716-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6716-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6716-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6716-114">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="b6716-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="b6716-115">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6716-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6716-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6716-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6716-117">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b6716-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b6716-118">*NumberOfSamples* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6716-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6716-119">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6716-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6716-120">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b6716-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6716-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6716-121">Return value</span></span>

<span data-ttu-id="b6716-122">Rien</span><span class="sxs-lookup"><span data-stu-id="b6716-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="b6716-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b6716-123">Remarks</span></span>

<span data-ttu-id="b6716-124">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b6716-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="b6716-125">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b6716-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b6716-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="b6716-126">Vertex</span></span> | <span data-ttu-id="b6716-127">Forme</span><span class="sxs-lookup"><span data-stu-id="b6716-127">Hull</span></span> | <span data-ttu-id="b6716-128">Domain</span><span class="sxs-lookup"><span data-stu-id="b6716-128">Domain</span></span> | <span data-ttu-id="b6716-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b6716-129">Geometry</span></span> | <span data-ttu-id="b6716-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="b6716-130">Pixel</span></span> | <span data-ttu-id="b6716-131">Compute</span><span class="sxs-lookup"><span data-stu-id="b6716-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b6716-132">x</span><span class="sxs-lookup"><span data-stu-id="b6716-132">x</span></span>     | <span data-ttu-id="b6716-133">x</span><span class="sxs-lookup"><span data-stu-id="b6716-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b6716-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6716-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6716-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b6716-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="b6716-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b6716-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

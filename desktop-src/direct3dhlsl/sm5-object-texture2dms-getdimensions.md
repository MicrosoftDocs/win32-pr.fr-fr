---
title: 'Texture2DMS :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DMS :: GetDimensions,, fonction'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953631"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="2559e-105">Texture2DMS :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="2559e-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="2559e-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="2559e-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2559e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2559e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="2559e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2559e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2559e-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2559e-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2559e-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2559e-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2559e-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="2559e-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2559e-112">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2559e-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2559e-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2559e-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2559e-114">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="2559e-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="2559e-115">*NumberOfSamples* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2559e-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2559e-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2559e-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2559e-117">Nombre d’emplacements d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="2559e-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2559e-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2559e-118">Return value</span></span>

<span data-ttu-id="2559e-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2559e-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2559e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2559e-120">Remarks</span></span>

<span data-ttu-id="2559e-121">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2559e-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="2559e-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2559e-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2559e-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="2559e-123">Vertex</span></span> | <span data-ttu-id="2559e-124">Forme</span><span class="sxs-lookup"><span data-stu-id="2559e-124">Hull</span></span> | <span data-ttu-id="2559e-125">Domain</span><span class="sxs-lookup"><span data-stu-id="2559e-125">Domain</span></span> | <span data-ttu-id="2559e-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2559e-126">Geometry</span></span> | <span data-ttu-id="2559e-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="2559e-127">Pixel</span></span> | <span data-ttu-id="2559e-128">Compute</span><span class="sxs-lookup"><span data-stu-id="2559e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2559e-129">x</span><span class="sxs-lookup"><span data-stu-id="2559e-129">x</span></span>     | <span data-ttu-id="2559e-130">x</span><span class="sxs-lookup"><span data-stu-id="2559e-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2559e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2559e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2559e-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="2559e-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="2559e-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2559e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

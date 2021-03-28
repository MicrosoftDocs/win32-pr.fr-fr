---
title: 'RWTexture3D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture3D :: GetDimensions,, fonction'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
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
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322162"
---
# <a name="rwtexture3dgetdimensions-function"></a><span data-ttu-id="c3ac3-105">RWTexture3D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="c3ac3-105">RWTexture3D::GetDimensions function</span></span>

<span data-ttu-id="c3ac3-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ac3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3ac3-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a><span data-ttu-id="c3ac3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3ac3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ac3-109">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3ac3-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ac3-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3ac3-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3ac3-111">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac3-112">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3ac3-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ac3-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3ac3-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3ac3-114">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac3-115">*Profondeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3ac3-115">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ac3-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3ac3-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3ac3-117">Profondeur des ressources, dans les texels.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-117">The resource depth, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ac3-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c3ac3-118">Return value</span></span>

<span data-ttu-id="c3ac3-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ac3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c3ac3-120">Remarks</span></span>

<span data-ttu-id="c3ac3-121">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c3ac3-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="c3ac3-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c3ac3-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3ac3-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="c3ac3-123">Vertex</span></span> | <span data-ttu-id="c3ac3-124">Forme</span><span class="sxs-lookup"><span data-stu-id="c3ac3-124">Hull</span></span> | <span data-ttu-id="c3ac3-125">Domain</span><span class="sxs-lookup"><span data-stu-id="c3ac3-125">Domain</span></span> | <span data-ttu-id="c3ac3-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c3ac3-126">Geometry</span></span> | <span data-ttu-id="c3ac3-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="c3ac3-127">Pixel</span></span> | <span data-ttu-id="c3ac3-128">Compute</span><span class="sxs-lookup"><span data-stu-id="c3ac3-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c3ac3-129">x</span><span class="sxs-lookup"><span data-stu-id="c3ac3-129">x</span></span>     | <span data-ttu-id="c3ac3-130">x</span><span class="sxs-lookup"><span data-stu-id="c3ac3-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3ac3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3ac3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ac3-132">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="c3ac3-132">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="c3ac3-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c3ac3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

---
title: 'Texture3D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture3D :: GetDimensions,, fonction'
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 7a700e0ff065e5f4758241ee0c8252965209a21f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992108"
---
# <a name="texture3dgetdimensions-function"></a><span data-ttu-id="e8d47-105">Texture3D :: GetDimensions,, fonction</span><span class="sxs-lookup"><span data-stu-id="e8d47-105">Texture3D::GetDimensions function</span></span>

<span data-ttu-id="e8d47-106">Retourne les dimensions de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e8d47-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8d47-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="e8d47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8d47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8d47-109">*MipLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8d47-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d47-110">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8d47-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8d47-111">facultatif.</span><span class="sxs-lookup"><span data-stu-id="e8d47-111">Optional.</span></span> <span data-ttu-id="e8d47-112">Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).</span><span class="sxs-lookup"><span data-stu-id="e8d47-112">Mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="e8d47-113">*Largeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8d47-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d47-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8d47-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8d47-115">Largeur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="e8d47-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e8d47-116">*Hauteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8d47-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d47-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8d47-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8d47-118">Hauteur des ressources, en texels.</span><span class="sxs-lookup"><span data-stu-id="e8d47-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e8d47-119">*Profondeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8d47-119">*Depth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d47-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8d47-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8d47-121">Profondeur des ressources, dans les texels.</span><span class="sxs-lookup"><span data-stu-id="e8d47-121">The resource depth, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="e8d47-122">*NumberOfLevels* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8d47-122">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d47-123">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8d47-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8d47-124">Nombre de niveaux de mipmap (requiert également *MipLevel* ).</span><span class="sxs-lookup"><span data-stu-id="e8d47-124">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8d47-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8d47-125">Return value</span></span>

<span data-ttu-id="e8d47-126">Rien</span><span class="sxs-lookup"><span data-stu-id="e8d47-126">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="e8d47-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e8d47-127">Remarks</span></span>

<span data-ttu-id="e8d47-128">Il s’agit d’une liste des versions surchargées de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e8d47-128">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



<span data-ttu-id="e8d47-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e8d47-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e8d47-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="e8d47-130">Vertex</span></span> | <span data-ttu-id="e8d47-131">Forme</span><span class="sxs-lookup"><span data-stu-id="e8d47-131">Hull</span></span> | <span data-ttu-id="e8d47-132">Domain</span><span class="sxs-lookup"><span data-stu-id="e8d47-132">Domain</span></span> | <span data-ttu-id="e8d47-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e8d47-133">Geometry</span></span> | <span data-ttu-id="e8d47-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="e8d47-134">Pixel</span></span> | <span data-ttu-id="e8d47-135">Compute</span><span class="sxs-lookup"><span data-stu-id="e8d47-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e8d47-136">x</span><span class="sxs-lookup"><span data-stu-id="e8d47-136">x</span></span>     | <span data-ttu-id="e8d47-137">x</span><span class="sxs-lookup"><span data-stu-id="e8d47-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e8d47-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8d47-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d47-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e8d47-139">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="e8d47-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e8d47-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

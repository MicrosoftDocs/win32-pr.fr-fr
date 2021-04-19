---
description: Caractéristiques du matériau de transfert de luminance (PRT) précalculées d’harmoniques sphériques (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: D3DXSHMATERIAL, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532437"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="27391-103">D3DXSHMATERIAL, structure</span><span class="sxs-lookup"><span data-stu-id="27391-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="27391-104">Caractéristiques du matériau de transfert de luminance (PRT) précalculées d’harmoniques sphériques (SH).</span><span class="sxs-lookup"><span data-stu-id="27391-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="27391-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27391-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="27391-106">Membres</span><span class="sxs-lookup"><span data-stu-id="27391-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27391-107">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="27391-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="27391-108">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-109">Albedo diffuse de l’aire.</span><span class="sxs-lookup"><span data-stu-id="27391-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="27391-110">Cette valeur est ignorée si l’objet est un miroir.</span><span class="sxs-lookup"><span data-stu-id="27391-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="27391-111">**bMirror**</span><span class="sxs-lookup"><span data-stu-id="27391-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="27391-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-113">Doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="27391-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="27391-114">**bSubSurf**</span><span class="sxs-lookup"><span data-stu-id="27391-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="27391-115">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-116">Affectez la valeur **true** pour activer la diffusion sous-surface ; tout objet qui effectue une diffusion sous-surface ne peut pas être un miroir.</span><span class="sxs-lookup"><span data-stu-id="27391-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="27391-117">**RelativeIndexOfRefraction**</span><span class="sxs-lookup"><span data-stu-id="27391-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="27391-118">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-119">L’index relatif de refraction correspond au rapport entre deux index absolus de réfraction.</span><span class="sxs-lookup"><span data-stu-id="27391-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="27391-120">Un index de réfraction est le rapport entre le sinus de l’angle d’incidence et le sinus de l’angle de réfraction.</span><span class="sxs-lookup"><span data-stu-id="27391-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="27391-121">**Absorption**</span><span class="sxs-lookup"><span data-stu-id="27391-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="27391-122">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-123">Le coefficient d’absorption est un paramètre de l’équation de rendu de volume utilisée pour modéliser la propagation de la lumière dans un support participant.</span><span class="sxs-lookup"><span data-stu-id="27391-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="27391-124">**ReducedScattering**</span><span class="sxs-lookup"><span data-stu-id="27391-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="27391-125">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="27391-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27391-126">Le coefficient de diffusion réduit est un paramètre de l’équation de rendu de volume utilisée pour modéliser la propagation de la lumière dans un support participant.</span><span class="sxs-lookup"><span data-stu-id="27391-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27391-127">Notes</span><span class="sxs-lookup"><span data-stu-id="27391-127">Remarks</span></span>

<span data-ttu-id="27391-128">Les scènes non spectrales utilisent le canal rouge à partir des matériaux au lieu de la valeur de luminance.</span><span class="sxs-lookup"><span data-stu-id="27391-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="27391-129">Pour plus d’informations sur PRT, consultez :</span><span class="sxs-lookup"><span data-stu-id="27391-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="27391-130">Jensen, Clément Wann, et al. SIGGRAPH, procédure : un modèle pratique pour le transport de lumière sous-surface, 2001.</span><span class="sxs-lookup"><span data-stu-id="27391-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="27391-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27391-131">Requirements</span></span>



| <span data-ttu-id="27391-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27391-132">Requirement</span></span> | <span data-ttu-id="27391-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="27391-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27391-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="27391-134">Header</span></span><br/> | <dl> <span data-ttu-id="27391-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="27391-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27391-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27391-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27391-137">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="27391-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

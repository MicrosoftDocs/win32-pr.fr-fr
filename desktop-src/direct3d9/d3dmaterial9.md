---
description: Spécifie les propriétés de matériau.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: D3DMATERIAL9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394156"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="347a1-103">D3DMATERIAL9, structure</span><span class="sxs-lookup"><span data-stu-id="347a1-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="347a1-104">Spécifie les propriétés de matériau.</span><span class="sxs-lookup"><span data-stu-id="347a1-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="347a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="347a1-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="347a1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="347a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="347a1-107">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="347a1-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="347a1-108">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="347a1-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="347a1-109">Valeur spécifiant la couleur diffuse du matériau.</span><span class="sxs-lookup"><span data-stu-id="347a1-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="347a1-110">Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="347a1-111">**Ambiant**</span><span class="sxs-lookup"><span data-stu-id="347a1-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="347a1-112">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="347a1-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="347a1-113">Valeur spécifiant la couleur ambiante du matériau.</span><span class="sxs-lookup"><span data-stu-id="347a1-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="347a1-114">Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="347a1-115">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="347a1-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="347a1-116">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="347a1-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="347a1-117">Valeur spécifiant la couleur spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="347a1-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="347a1-118">Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="347a1-119">**Émissif**</span><span class="sxs-lookup"><span data-stu-id="347a1-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="347a1-120">Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="347a1-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="347a1-121">Valeur spécifiant la couleur émissif du matériau.</span><span class="sxs-lookup"><span data-stu-id="347a1-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="347a1-122">Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="347a1-123">**Power**</span><span class="sxs-lookup"><span data-stu-id="347a1-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="347a1-124">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="347a1-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="347a1-125">Valeur à virgule flottante spécifiant la netteté des surbrillances spéculaires.</span><span class="sxs-lookup"><span data-stu-id="347a1-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="347a1-126">Plus la valeur est élevée, plus la mise en surbrillance est nette.</span><span class="sxs-lookup"><span data-stu-id="347a1-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="347a1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="347a1-127">Remarks</span></span>

<span data-ttu-id="347a1-128">Pour désactiver les surbrillances spéculaires, affectez la valeur \_ **false** à D3DRS SpecularEnable, à l’aide de [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="347a1-129">Il s’agit de l’option la plus rapide car aucune surbrillance spéculaire n’est calculée.</span><span class="sxs-lookup"><span data-stu-id="347a1-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="347a1-130">Pour plus d’informations sur l’utilisation du moteur d’éclairage pour calculer l’éclairage spéculaire, consultez [éclairage spéculaire (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="347a1-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="347a1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="347a1-131">Requirements</span></span>



| <span data-ttu-id="347a1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="347a1-132">Requirement</span></span> | <span data-ttu-id="347a1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="347a1-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="347a1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="347a1-134">Header</span></span><br/> | <dl> <span data-ttu-id="347a1-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="347a1-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347a1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="347a1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347a1-137">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="347a1-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="347a1-138">**IDirect3DDevice9::GetMaterial**</span><span class="sxs-lookup"><span data-stu-id="347a1-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="347a1-139">**IDirect3DDevice9::SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="347a1-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 

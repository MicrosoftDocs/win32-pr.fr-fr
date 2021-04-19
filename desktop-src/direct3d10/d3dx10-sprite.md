---
description: Définit les informations relatives à la position, à la texture et à la couleur d’un sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Structure D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529629"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="7e88f-103">D3DX10, \_ structure</span><span class="sxs-lookup"><span data-stu-id="7e88f-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="7e88f-104">Définit les informations relatives à la position, à la texture et à la couleur d’un sprite.</span><span class="sxs-lookup"><span data-stu-id="7e88f-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e88f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e88f-105">Syntax</span></span>


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a><span data-ttu-id="7e88f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7e88f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e88f-107">**matWorld**</span><span class="sxs-lookup"><span data-stu-id="7e88f-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-109">Transformation universelle du modèle du sprite.</span><span class="sxs-lookup"><span data-stu-id="7e88f-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="7e88f-110">Cela définit la position et l’orientation du sprite dans l’espace universel.</span><span class="sxs-lookup"><span data-stu-id="7e88f-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="7e88f-111">**TexCoord**</span><span class="sxs-lookup"><span data-stu-id="7e88f-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-112">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88f-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-113">Décalage à partir de l’angle supérieur gauche de la texture indiquant l’emplacement où l’image du sprite doit commencer dans la texture.</span><span class="sxs-lookup"><span data-stu-id="7e88f-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="7e88f-114">**TexCoord** est en coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7e88f-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7e88f-115">**TexSize**</span><span class="sxs-lookup"><span data-stu-id="7e88f-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-116">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88f-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-117">Vecteur contenant la largeur et la hauteur du sprite dans les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7e88f-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7e88f-118">**ColorModulate**</span><span class="sxs-lookup"><span data-stu-id="7e88f-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-119">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88f-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-120">Couleur qui sera multipliée par la couleur de pixel avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="7e88f-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="7e88f-121">**pTexture**</span><span class="sxs-lookup"><span data-stu-id="7e88f-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-122">Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="7e88f-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-123">Pointeur vers une vue de la ressource Shader qui représente la texture du sprite.</span><span class="sxs-lookup"><span data-stu-id="7e88f-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="7e88f-124">Voir [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="7e88f-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="7e88f-125">**TextureIndex**</span><span class="sxs-lookup"><span data-stu-id="7e88f-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="7e88f-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e88f-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e88f-127">Index de la texture.</span><span class="sxs-lookup"><span data-stu-id="7e88f-127">The index of the texture.</span></span> <span data-ttu-id="7e88f-128">Si pTexture ne représente pas un tableau de texture, la valeur doit être 0.</span><span class="sxs-lookup"><span data-stu-id="7e88f-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e88f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e88f-129">Requirements</span></span>



| <span data-ttu-id="7e88f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e88f-130">Requirement</span></span> | <span data-ttu-id="7e88f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e88f-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e88f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e88f-132">Header</span></span><br/> | <dl> <span data-ttu-id="7e88f-133"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e88f-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e88f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e88f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e88f-135">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="7e88f-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

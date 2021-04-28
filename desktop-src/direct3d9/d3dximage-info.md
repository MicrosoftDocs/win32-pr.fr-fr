---
description: D3DXIMAGE_INFO structure-retourne une description du contenu d’origine d’un fichier image.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Structure D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090537"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="9c5f1-103">\_Structure d’informations D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="9c5f1-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="9c5f1-104">Retourne une description du contenu d’origine d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c5f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c5f1-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="9c5f1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9c5f1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c5f1-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-109">Largeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-112">Hauteur de l’image d’origine en pixels.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-113">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-115">Profondeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-116">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-118">Nombre de niveaux MIP dans l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-119">**Format**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-120">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-121">Valeur du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le plus précisément les données de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-123">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-124">Représente le type de la texture stockée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="9c5f1-125">Il s’agit de D3DRTYPE \_ texture, D3DRTYPE \_ VOLUMETEXTURE ou D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="9c5f1-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9c5f1-127">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9c5f1-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9c5f1-128">Représente le format du fichier image.</span><span class="sxs-lookup"><span data-stu-id="9c5f1-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c5f1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c5f1-129">Requirements</span></span>



| <span data-ttu-id="9c5f1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c5f1-130">Requirement</span></span> | <span data-ttu-id="9c5f1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c5f1-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5f1-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c5f1-132">Header</span></span><br/> | <dl> <span data-ttu-id="9c5f1-133"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c5f1-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c5f1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c5f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c5f1-135">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="9c5f1-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

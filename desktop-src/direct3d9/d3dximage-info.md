---
description: Retourne une description du contenu d’origine d’un fichier image.
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
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762037"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="9da92-103">\_Structure d’informations D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="9da92-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="9da92-104">Retourne une description du contenu d’origine d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="9da92-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9da92-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="9da92-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9da92-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9da92-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="9da92-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-109">Largeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9da92-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="9da92-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-112">Hauteur de l’image d’origine en pixels.</span><span class="sxs-lookup"><span data-stu-id="9da92-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-113">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="9da92-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-115">Profondeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9da92-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-116">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="9da92-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-118">Nombre de niveaux MIP dans l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="9da92-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-119">**Format**</span><span class="sxs-lookup"><span data-stu-id="9da92-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-120">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-121">Valeur du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le plus précisément les données de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="9da92-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9da92-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-123">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-124">Représente le type de la texture stockée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9da92-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="9da92-125">Il s’agit de D3DRTYPE \_ texture, D3DRTYPE \_ VOLUMETEXTURE ou D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="9da92-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="9da92-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="9da92-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9da92-127">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9da92-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9da92-128">Représente le format du fichier image.</span><span class="sxs-lookup"><span data-stu-id="9da92-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9da92-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9da92-129">Requirements</span></span>



| <span data-ttu-id="9da92-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9da92-130">Requirement</span></span> | <span data-ttu-id="9da92-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9da92-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9da92-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9da92-132">Header</span></span><br/> | <dl> <span data-ttu-id="9da92-133"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9da92-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da92-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9da92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da92-135">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="9da92-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

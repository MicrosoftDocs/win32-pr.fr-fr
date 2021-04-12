---
description: Retourne une description du contenu d’origine d’un fichier image.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Structure D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322753"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="ee4c6-103">Structure d’informations d' \_ image d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="ee4c6-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="ee4c6-104">Retourne une description du contenu d’origine d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee4c6-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="ee4c6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ee4c6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee4c6-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-109">Largeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-112">Hauteur de l’image d’origine en pixels.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-113">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-115">Profondeur de l’image d’origine, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-118">Taille du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-118">Size of the texture array.</span></span> <span data-ttu-id="ee4c6-119">*ArraySize* sera 1 pour une seule image.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-120">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-122">Nombre de niveaux de mipmap dans l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-125">Diverses propriétés de ressource ( [**consultez \_ \_ \_ indicateur divers des ressources D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-126">**Format**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-127">Type : **[ **dxgi \_ format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-128">Valeur du type énuméré [**de \_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) qui décrit le plus précisément les données de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-130">Type : **[ **\_ \_ dimension de ressource D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-131">Représente le type de la texture stockée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="ee4c6-132">Consultez [**\_ \_ dimension de ressource D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="ee4c6-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ee4c6-134">Type : **[ **d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="ee4c6-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ee4c6-135">Représente le format du fichier image.</span><span class="sxs-lookup"><span data-stu-id="ee4c6-135">Represents the format of the image file.</span></span> <span data-ttu-id="ee4c6-136">Consultez [**\_ format de \_ fichier \_ image d3dx10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="ee4c6-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee4c6-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee4c6-137">Requirements</span></span>



| <span data-ttu-id="ee4c6-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee4c6-138">Requirement</span></span> | <span data-ttu-id="ee4c6-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee4c6-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4c6-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee4c6-140">Header</span></span><br/> | <dl> <span data-ttu-id="ee4c6-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4c6-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4c6-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee4c6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4c6-143">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="ee4c6-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

---
title: Structure D3DX11_IMAGE_INFO (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. | Structure D3DX11_IMAGE_INFO (D3DX11tex. h)'
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Structure D3DX11_IMAGE_INFO Direct3D 11
- Pointeur de structure LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982559"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="b41ce-107">Structure d’informations d' \_ image D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="b41ce-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="b41ce-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b41ce-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="b41ce-109">Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées.</span><span class="sxs-lookup"><span data-stu-id="b41ce-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="b41ce-110">\_La valeur par défaut D3DX11 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.</span><span class="sxs-lookup"><span data-stu-id="b41ce-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b41ce-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b41ce-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="b41ce-112">Membres</span><span class="sxs-lookup"><span data-stu-id="b41ce-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="b41ce-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="b41ce-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-115">Largeur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="b41ce-115">The target width of the texture.</span></span> <span data-ttu-id="b41ce-116">Si la largeur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette largeur cible.</span><span class="sxs-lookup"><span data-stu-id="b41ce-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="b41ce-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-119">Hauteur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="b41ce-119">The target height of the texture.</span></span> <span data-ttu-id="b41ce-120">Si la hauteur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette hauteur cible.</span><span class="sxs-lookup"><span data-stu-id="b41ce-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-121">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="b41ce-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-122">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-123">Profondeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="b41ce-123">The depth of the texture.</span></span> <span data-ttu-id="b41ce-124">Cela s’applique uniquement aux textures de volume.</span><span class="sxs-lookup"><span data-stu-id="b41ce-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="b41ce-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-126">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-127">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b41ce-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-128">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="b41ce-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-129">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-130">Nombre maximal de niveaux de mipmap dans la texture.</span><span class="sxs-lookup"><span data-stu-id="b41ce-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="b41ce-131">Consultez les notes dans [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="b41ce-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="b41ce-132">L’utilisation de \_ la valeur par défaut 0 ou D3DX11 entraîne la création d’une chaîne mipmap complète.</span><span class="sxs-lookup"><span data-stu-id="b41ce-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-133">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="b41ce-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-134">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-135">Diverses propriétés de ressource spécifiées avec un indicateur d' [**\_ \_ \_ indicateur div de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="b41ce-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="b41ce-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-137">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-138">Énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) spécifiant le format de la texture après son chargement.</span><span class="sxs-lookup"><span data-stu-id="b41ce-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-139">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="b41ce-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-140">Type : **[ **\_ \_ dimension de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-141">Valeur [**de \_ \_ dimension de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , qui identifie le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="b41ce-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="b41ce-142">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="b41ce-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="b41ce-143">Type : **[ **D3DX11 \_ image \_ file \_ format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="b41ce-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b41ce-144">Valeur [**de \_ \_ \_ format de fichier image D3DX11**](d3dx11-image-file-format.md) , qui identifie le format de l’image.</span><span class="sxs-lookup"><span data-stu-id="b41ce-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b41ce-145">Notes</span><span class="sxs-lookup"><span data-stu-id="b41ce-145">Remarks</span></span>

<span data-ttu-id="b41ce-146">Cette structure est utilisée par les méthodes telles que : [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="b41ce-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b41ce-147">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b41ce-147">Requirements</span></span>



| <span data-ttu-id="b41ce-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b41ce-148">Requirement</span></span> | <span data-ttu-id="b41ce-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="b41ce-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b41ce-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="b41ce-150">Header</span></span><br/> | <dl> <span data-ttu-id="b41ce-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41ce-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41ce-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b41ce-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41ce-153">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="b41ce-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 


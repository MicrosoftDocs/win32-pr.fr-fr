---
description: Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. \_La valeur par défaut d3dx10 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Structure D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522382"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="0f909-104">\_Structure des \_ informations de chargement d’image d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="0f909-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="0f909-105">Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées.</span><span class="sxs-lookup"><span data-stu-id="0f909-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="0f909-106">\_La valeur par défaut d3dx10 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.</span><span class="sxs-lookup"><span data-stu-id="0f909-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f909-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f909-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="0f909-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0f909-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f909-109">**Width**</span><span class="sxs-lookup"><span data-stu-id="0f909-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-111">Largeur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="0f909-111">The target width of the texture.</span></span> <span data-ttu-id="0f909-112">Si la largeur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette largeur cible.</span><span class="sxs-lookup"><span data-stu-id="0f909-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-113">**Height**</span><span class="sxs-lookup"><span data-stu-id="0f909-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-115">Hauteur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="0f909-115">The target height of the texture.</span></span> <span data-ttu-id="0f909-116">Si la hauteur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette hauteur cible.</span><span class="sxs-lookup"><span data-stu-id="0f909-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-117">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="0f909-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-119">Profondeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="0f909-119">The depth of the texture.</span></span> <span data-ttu-id="0f909-120">Cela s’applique uniquement aux textures de volume.</span><span class="sxs-lookup"><span data-stu-id="0f909-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-121">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="0f909-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-123">Niveau de mipmap de résolution le plus élevé de la texture.</span><span class="sxs-lookup"><span data-stu-id="0f909-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="0f909-124">Si la valeur est supérieure à 0, après le chargement de la texture, FirstMipLevel est mappé au niveau mipmap 0.</span><span class="sxs-lookup"><span data-stu-id="0f909-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-125">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="0f909-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-127">Nombre maximal de niveaux de mipmap que la texture aura.</span><span class="sxs-lookup"><span data-stu-id="0f909-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="0f909-128">L’utilisation de \_ la valeur par défaut 0 ou d3dx10 entraîne la création d’une chaîne mipmap complète.</span><span class="sxs-lookup"><span data-stu-id="0f909-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="0f909-129">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="0f909-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-130">Type : **[ **\_ utilisation de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="0f909-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-131">La façon dont la ressource de texture est destinée à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0f909-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="0f909-132">Consultez [**\_ utilisation de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="0f909-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="0f909-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-134">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-135">Étapes de pipeline que la texture sera autorisée à lier.</span><span class="sxs-lookup"><span data-stu-id="0f909-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="0f909-136">Consultez [**l' \_ \_ indicateur de liaison D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="0f909-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-137">**Cpuaccessflags a**</span><span class="sxs-lookup"><span data-stu-id="0f909-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-138">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-139">Autorisations d’accès dont dispose l’UC pour la ressource de texture.</span><span class="sxs-lookup"><span data-stu-id="0f909-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="0f909-140">Consultez [**\_ indicateur d' \_ accès \_ au processeur D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="0f909-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-141">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="0f909-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-142">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-143">Diverses propriétés de ressource ( [**consultez \_ \_ \_ indicateur divers des ressources D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="0f909-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-144">**Format**</span><span class="sxs-lookup"><span data-stu-id="0f909-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-145">Type : **[ **dxgi \_ format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0f909-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-146">Format de la texture après son chargement.</span><span class="sxs-lookup"><span data-stu-id="0f909-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="0f909-147">Consultez [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="0f909-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="0f909-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-149">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-150">Filtre la texture à l’aide du filtre spécifié (uniquement lors du rééchantillonnage).</span><span class="sxs-lookup"><span data-stu-id="0f909-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="0f909-151">Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="0f909-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-153">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f909-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f909-154">Filtrez les niveaux MIP de texture à l’aide du filtre spécifié (uniquement si vous générez des mipmaps).</span><span class="sxs-lookup"><span data-stu-id="0f909-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="0f909-155">Les valeurs valides sont le \_ filtre d3dx10 \_ aucun, le \_ point de filtre d3dx10, le filtre d3dx10 de filtre \_ \_ \_ linéaire ou le \_ triangle de filtre d3dx10 \_ .</span><span class="sxs-lookup"><span data-stu-id="0f909-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="0f909-156">Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f909-157">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="0f909-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0f909-158">Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f909-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="0f909-159">Informations sur l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="0f909-159">Information about the original image.</span></span> <span data-ttu-id="0f909-160">Consultez [**d3dx10 \_ image \_ info**](d3dx10-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="0f909-161">Peut être obtenu avec [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)ou [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f909-162">Notes</span><span class="sxs-lookup"><span data-stu-id="0f909-162">Remarks</span></span>

<span data-ttu-id="0f909-163">Lors de l’initialisation de la structure, vous pouvez définir n’importe quel membre sur D3DX10 \_ par défaut et D3DX l’initialise avec une valeur par défaut à partir de la texture source lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="0f909-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="0f909-164">Cette structure peut être utilisée par les API qui :</span><span class="sxs-lookup"><span data-stu-id="0f909-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="0f909-165">Créer des ressources, telles que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="0f909-166">Créer des processeurs de données, tels que [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) ou [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="0f909-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f909-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f909-167">Requirements</span></span>



| <span data-ttu-id="0f909-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f909-168">Requirement</span></span> | <span data-ttu-id="0f909-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f909-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f909-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f909-170">Header</span></span><br/> | <dl> <span data-ttu-id="0f909-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f909-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f909-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f909-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f909-173">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="0f909-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

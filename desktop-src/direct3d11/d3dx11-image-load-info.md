---
title: Structure D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. | Structure D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)'
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- Structure D3DX11_IMAGE_LOAD_INFO Direct3D 11
- Pointeur de structure LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982554"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="eaba2-107">\_Structure des \_ informations de chargement d’image D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="eaba2-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="eaba2-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eaba2-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="eaba2-109">Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées.</span><span class="sxs-lookup"><span data-stu-id="eaba2-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="eaba2-110">\_La valeur par défaut D3DX11 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.</span><span class="sxs-lookup"><span data-stu-id="eaba2-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaba2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaba2-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="eaba2-112">Membres</span><span class="sxs-lookup"><span data-stu-id="eaba2-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="eaba2-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="eaba2-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-115">Largeur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-115">The target width of the texture.</span></span> <span data-ttu-id="eaba2-116">Si la largeur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette largeur cible.</span><span class="sxs-lookup"><span data-stu-id="eaba2-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="eaba2-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-119">Hauteur cible de la texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-119">The target height of the texture.</span></span> <span data-ttu-id="eaba2-120">Si la hauteur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette hauteur cible.</span><span class="sxs-lookup"><span data-stu-id="eaba2-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-121">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="eaba2-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-122">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-123">Profondeur de la texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-123">The depth of the texture.</span></span> <span data-ttu-id="eaba2-124">Cela s’applique uniquement aux textures de volume.</span><span class="sxs-lookup"><span data-stu-id="eaba2-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-125">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="eaba2-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-126">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-127">Niveau de mipmap de résolution le plus élevé de la texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="eaba2-128">Si la valeur est supérieure à 0, après le chargement de la texture, FirstMipLevel est mappé au niveau mipmap 0.</span><span class="sxs-lookup"><span data-stu-id="eaba2-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-129">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="eaba2-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-130">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-131">Nombre maximal de niveaux de mipmap dans la texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="eaba2-132">Consultez les notes dans [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="eaba2-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="eaba2-133">L’utilisation de \_ la valeur par défaut 0 ou D3DX11 entraîne la création d’une chaîne mipmap complète.</span><span class="sxs-lookup"><span data-stu-id="eaba2-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-134">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="eaba2-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-135">Type : **[ **\_ utilisation de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-136">La façon dont la ressource de texture est destinée à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="eaba2-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="eaba2-137">Consultez [**\_ utilisation de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="eaba2-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="eaba2-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-139">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-140">Étapes de pipeline que la texture sera autorisée à lier.</span><span class="sxs-lookup"><span data-stu-id="eaba2-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="eaba2-141">Consultez [**l' \_ \_ indicateur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="eaba2-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-142">**Cpuaccessflags a**</span><span class="sxs-lookup"><span data-stu-id="eaba2-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-143">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-144">Autorisations d’accès dont dispose l’UC pour la ressource de texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="eaba2-145">Consultez [**\_ indicateur d' \_ accès \_ au processeur d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="eaba2-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-146">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="eaba2-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-147">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-148">Diverses propriétés de ressource ( [**consultez \_ \_ \_ indicateur divers des ressources d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="eaba2-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-149">**Format**</span><span class="sxs-lookup"><span data-stu-id="eaba2-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-150">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-151">Énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indiquant le format de la texture après son chargement.</span><span class="sxs-lookup"><span data-stu-id="eaba2-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-152">**Filter**</span><span class="sxs-lookup"><span data-stu-id="eaba2-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-153">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-154">Filtre la texture à l’aide du filtre spécifié (uniquement lors du rééchantillonnage).</span><span class="sxs-lookup"><span data-stu-id="eaba2-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="eaba2-155">Consultez [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="eaba2-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-157">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaba2-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-158">Filtrez les niveaux MIP de texture à l’aide du filtre spécifié (uniquement si vous générez des mipmaps).</span><span class="sxs-lookup"><span data-stu-id="eaba2-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="eaba2-159">Les valeurs valides sont le \_ filtre D3DX11 \_ aucun, le \_ point de filtre D3DX11, le filtre D3DX11 de filtre \_ \_ \_ linéaire ou le \_ triangle de filtre D3DX11 \_ .</span><span class="sxs-lookup"><span data-stu-id="eaba2-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="eaba2-160">Consultez [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaba2-161">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="eaba2-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="eaba2-162">Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="eaba2-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="eaba2-163">Informations sur l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="eaba2-163">Information about the original image.</span></span> <span data-ttu-id="eaba2-164">Consultez [**D3DX11 \_ image \_ info**](d3dx11-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="eaba2-165">Peut être obtenu avec [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaba2-166">Notes</span><span class="sxs-lookup"><span data-stu-id="eaba2-166">Remarks</span></span>

<span data-ttu-id="eaba2-167">Lors de l’initialisation de la structure, vous pouvez définir n’importe quel membre sur D3DX11 \_ par défaut et D3DX l’initialise avec une valeur par défaut à partir de la texture source lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="eaba2-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="eaba2-168">Cette structure peut être utilisée par les API qui :</span><span class="sxs-lookup"><span data-stu-id="eaba2-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="eaba2-169">Créer des ressources, telles que [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="eaba2-170">Créer des processeurs de données, tels que [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) ou [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="eaba2-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="eaba2-171">Les valeurs par défaut sont :</span><span class="sxs-lookup"><span data-stu-id="eaba2-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="eaba2-172">Voici un bref exemple qui utilise cette structure pour fournir le format de pixel lors du chargement d’une texture.</span><span class="sxs-lookup"><span data-stu-id="eaba2-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="eaba2-173">Pour obtenir le code complet, consultez HDRFormats10. cpp dans l' [exemple HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="eaba2-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="eaba2-174">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eaba2-174">Requirements</span></span>



| <span data-ttu-id="eaba2-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaba2-175">Requirement</span></span> | <span data-ttu-id="eaba2-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaba2-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaba2-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="eaba2-177">Header</span></span><br/> | <dl> <span data-ttu-id="eaba2-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaba2-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaba2-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaba2-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaba2-180">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="eaba2-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 


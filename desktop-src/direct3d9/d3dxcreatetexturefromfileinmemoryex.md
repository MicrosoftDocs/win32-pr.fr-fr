---
description: Crée une texture à partir d’un fichier en mémoire. Il s’agit d’une fonction plus avancée que D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: D3DXCreateTextureFromFileInMemoryEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953858"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="659f0-104">D3DXCreateTextureFromFileInMemoryEx fonction)</span><span class="sxs-lookup"><span data-stu-id="659f0-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="659f0-105">Crée une texture à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="659f0-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="659f0-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="659f0-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="659f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="659f0-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="659f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="659f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="659f0-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="659f0-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="659f0-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="659f0-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-113">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-114">Pointeur vers le fichier en mémoire à partir duquel créer la texture.</span><span class="sxs-lookup"><span data-stu-id="659f0-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-115">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-117">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="659f0-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-118">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-120">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="659f0-120">Width in pixels.</span></span> <span data-ttu-id="659f0-121">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="659f0-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-122">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-124">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="659f0-124">Height, in pixels.</span></span> <span data-ttu-id="659f0-125">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="659f0-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-126">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-128">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="659f0-128">Number of mip levels requested.</span></span> <span data-ttu-id="659f0-129">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="659f0-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-130">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-132">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="659f0-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="659f0-133">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="659f0-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="659f0-134">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="659f0-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="659f0-135">Si D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="659f0-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="659f0-136">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="659f0-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="659f0-137">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-138">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="659f0-139">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="659f0-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="659f0-140">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="659f0-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="659f0-141">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="659f0-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="659f0-142">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="659f0-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="659f0-143">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="659f0-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-144">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-145">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="659f0-146">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="659f0-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-147">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-148">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-149">Combinaison d’un ou plusieurs indicateurs contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="659f0-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="659f0-150">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="659f0-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="659f0-151">Chaque filtre valide doit contenir l’un des indicateurs dans [le \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="659f0-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="659f0-152">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-153">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="659f0-154">Combinaison d’un ou plusieurs indicateurs contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="659f0-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="659f0-155">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="659f0-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="659f0-156">Chaque filtre valide doit contenir l’un des indicateurs dans [le \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="659f0-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="659f0-157">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="659f0-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-158">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="659f0-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-159">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="659f0-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="659f0-160">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="659f0-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="659f0-161">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="659f0-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="659f0-162">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="659f0-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="659f0-163">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="659f0-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-164">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="659f0-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-165">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="659f0-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="659f0-166">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="659f0-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-167">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="659f0-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-168">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="659f0-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="659f0-169">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="659f0-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="659f0-170">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="659f0-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="659f0-171">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="659f0-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659f0-172">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="659f0-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="659f0-173">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="659f0-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="659f0-174">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="659f0-174">Return value</span></span>

<span data-ttu-id="659f0-175">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="659f0-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="659f0-176">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="659f0-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="659f0-177">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="659f0-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="659f0-178">Notes</span><span class="sxs-lookup"><span data-stu-id="659f0-178">Remarks</span></span>

<span data-ttu-id="659f0-179">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="659f0-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="659f0-180">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="659f0-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="659f0-181">Pour plus d’informations sur [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="659f0-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="659f0-182">Notez que à compter de DirectX 8,0, le membre peFlags de la structure **PaletteEntry** ne fonctionne pas comme décrit dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="659f0-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="659f0-183">Le membre peFlags est maintenant le canal alpha pour les formats en palette de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="659f0-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="659f0-184">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter.</span><span class="sxs-lookup"><span data-stu-id="659f0-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="659f0-185">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.</span><span class="sxs-lookup"><span data-stu-id="659f0-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="659f0-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="659f0-186">Requirements</span></span>



| <span data-ttu-id="659f0-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="659f0-187">Requirement</span></span> | <span data-ttu-id="659f0-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="659f0-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="659f0-189">En-tête</span><span class="sxs-lookup"><span data-stu-id="659f0-189">Header</span></span><br/>  | <dl> <span data-ttu-id="659f0-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="659f0-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="659f0-191">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="659f0-191">Library</span></span><br/> | <dl> <span data-ttu-id="659f0-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="659f0-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="659f0-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="659f0-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659f0-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="659f0-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="659f0-195">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="659f0-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

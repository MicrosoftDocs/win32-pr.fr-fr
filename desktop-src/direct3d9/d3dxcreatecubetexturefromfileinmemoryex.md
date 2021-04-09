---
description: Crée une texture de cube à partir d’un fichier en mémoire. Il s’agit d’une fonction plus avancée que D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: D3DXCreateCubeTextureFromFileInMemoryEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043168"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="ab655-104">D3DXCreateCubeTextureFromFileInMemoryEx fonction)</span><span class="sxs-lookup"><span data-stu-id="ab655-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="ab655-105">Crée une texture de cube à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ab655-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="ab655-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ab655-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab655-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab655-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ab655-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab655-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab655-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ab655-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ab655-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="ab655-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-113">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-114">Pointeur vers le fichier en mémoire à partir duquel créer la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="ab655-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="ab655-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ab655-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-116">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-118">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="ab655-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-119">*Taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-121">Largeur (ou hauteur) en pixels.</span><span class="sxs-lookup"><span data-stu-id="ab655-121">Width (or height) in pixels.</span></span> <span data-ttu-id="ab655-122">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="ab655-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-123">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-125">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="ab655-125">Number of mip levels requested.</span></span> <span data-ttu-id="ab655-126">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="ab655-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-127">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-129">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="ab655-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ab655-130">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="ab655-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ab655-131">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ab655-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ab655-132">Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ab655-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ab655-133">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ab655-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab655-134">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-135">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ab655-136">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="ab655-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="ab655-137">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="ab655-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ab655-138">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="ab655-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="ab655-139">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="ab655-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ab655-140">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab655-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-141">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-142">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ab655-143">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture de cube doit être placée.</span><span class="sxs-lookup"><span data-stu-id="ab655-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-144">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-145">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-146">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="ab655-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ab655-147">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab655-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-148">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-149">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab655-150">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="ab655-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ab655-151">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ab655-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="ab655-152">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="ab655-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-153">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab655-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-154">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ab655-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ab655-155">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="ab655-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ab655-156">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="ab655-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ab655-157">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="ab655-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ab655-158">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ab655-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-159">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab655-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-160">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab655-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ab655-161">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ab655-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-162">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ab655-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-163">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ab655-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ab655-164">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ab655-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="ab655-165">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ab655-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab655-166">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ab655-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab655-167">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ab655-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="ab655-168">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="ab655-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab655-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab655-169">Return value</span></span>

<span data-ttu-id="ab655-170">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab655-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab655-171">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab655-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab655-172">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab655-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab655-173">Notes</span><span class="sxs-lookup"><span data-stu-id="ab655-173">Remarks</span></span>

<span data-ttu-id="ab655-174">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="ab655-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ab655-175">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ab655-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ab655-176">Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces.</span><span class="sxs-lookup"><span data-stu-id="ab655-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="ab655-177">Pour appeler [**SetRenderTarget**](/windows/desktop/api) avec une texture de cube, vous devez sélectionner un visage individuel à l’aide de [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) et passer la surface résultante à **SetRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="ab655-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="ab655-178">Cette méthode est conçue pour être utilisée pour charger des fichiers image stockés en tant que RT \_ RCDATA, qui est une ressource définie par l’application (données brutes).</span><span class="sxs-lookup"><span data-stu-id="ab655-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="ab655-179">Dans le cas contraire, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="ab655-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="ab655-180">Pour plus d’informations sur [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ab655-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="ab655-181">Notez que à compter de DirectX 8,0, le membre peFlags de la structure **PaletteEntry** ne fonctionne pas comme décrit dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ab655-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="ab655-182">Le membre peFlags est maintenant le canal alpha pour les formats en palette de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="ab655-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="ab655-183">**D3DXCreateCubeTextureFromFileInMemoryEx** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="ab655-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="ab655-184">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="ab655-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="ab655-185">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="ab655-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="ab655-186">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="ab655-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="ab655-187">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter.</span><span class="sxs-lookup"><span data-stu-id="ab655-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="ab655-188">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.</span><span class="sxs-lookup"><span data-stu-id="ab655-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab655-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab655-189">Requirements</span></span>



| <span data-ttu-id="ab655-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab655-190">Requirement</span></span> | <span data-ttu-id="ab655-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab655-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab655-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab655-192">Header</span></span><br/>  | <dl> <span data-ttu-id="ab655-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab655-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ab655-194">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab655-194">Library</span></span><br/> | <dl> <span data-ttu-id="ab655-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab655-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ab655-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab655-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab655-197">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ab655-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

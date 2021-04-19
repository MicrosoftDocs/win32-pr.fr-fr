---
description: Crée une texture de volume à partir d’un fichier. Il s’agit d’une fonction plus avancée que D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: D3DXCreateVolumeTextureFromFileInMemoryEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538334"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a><span data-ttu-id="2423e-104">D3DXCreateVolumeTextureFromFileInMemoryEx fonction)</span><span class="sxs-lookup"><span data-stu-id="2423e-104">D3DXCreateVolumeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="2423e-105">Crée une texture de volume à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="2423e-105">Creates a volume texture from a file.</span></span> <span data-ttu-id="2423e-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="2423e-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2423e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2423e-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2423e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2423e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2423e-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2423e-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2423e-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="2423e-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-113">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-114">Pointeur vers le fichier en mémoire à partir duquel créer la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="2423e-114">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-115">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-117">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="2423e-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-118">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-120">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="2423e-120">Width in pixels.</span></span> <span data-ttu-id="2423e-121">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2423e-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2423e-122">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2423e-122">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2423e-123">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-125">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2423e-125">Height, in pixels.</span></span> <span data-ttu-id="2423e-126">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2423e-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2423e-127">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2423e-127">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2423e-128">*Profondeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-128">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-130">Profondeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2423e-130">Depth, in pixels.</span></span> <span data-ttu-id="2423e-131">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2423e-131">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2423e-132">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2423e-132">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2423e-133">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-133">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-134">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-135">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="2423e-135">Number of mip levels requested.</span></span> <span data-ttu-id="2423e-136">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="2423e-136">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-137">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-137">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-138">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-139">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="2423e-139">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2423e-140">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="2423e-140">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2423e-141">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="2423e-141">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="2423e-142">Si D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2423e-142">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2423e-143">D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="2423e-143">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="2423e-144">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="2423e-144">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="2423e-145">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-145">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-146">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-146">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2423e-147">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="2423e-147">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="2423e-148">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="2423e-148">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2423e-149">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="2423e-149">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="2423e-150">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="2423e-150">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="2423e-151">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2423e-151">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-152">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-152">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-153">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-153">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2423e-154">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="2423e-154">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-155">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-155">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-156">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-157">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="2423e-157">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2423e-158">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2423e-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-159">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-159">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-160">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-160">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2423e-161">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="2423e-161">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2423e-162">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="2423e-162">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="2423e-163">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="2423e-163">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-164">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2423e-164">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-165">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2423e-165">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2423e-166">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="2423e-166">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2423e-167">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="2423e-167">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2423e-168">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="2423e-168">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2423e-169">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="2423e-169">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-170">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2423e-170">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-171">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2423e-171">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2423e-172">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="2423e-172">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-173">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2423e-173">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-174">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="2423e-174">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2423e-175">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="2423e-175">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2423e-176">*ppVolumeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2423e-176">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2423e-177">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2423e-177">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="2423e-178">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="2423e-178">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2423e-179">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2423e-179">Return value</span></span>

<span data-ttu-id="2423e-180">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2423e-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2423e-181">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2423e-181">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2423e-182">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2423e-182">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2423e-183">Notes</span><span class="sxs-lookup"><span data-stu-id="2423e-183">Remarks</span></span>

<span data-ttu-id="2423e-184">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="2423e-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2423e-185">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2423e-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2423e-186">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="2423e-186">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="2423e-187">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="2423e-187">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2423e-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2423e-188">Requirements</span></span>



| <span data-ttu-id="2423e-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2423e-189">Requirement</span></span> | <span data-ttu-id="2423e-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="2423e-190">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2423e-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="2423e-191">Header</span></span><br/>  | <dl> <span data-ttu-id="2423e-192"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2423e-192"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2423e-193">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2423e-193">Library</span></span><br/> | <dl> <span data-ttu-id="2423e-194"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2423e-194"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2423e-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2423e-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2423e-196">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="2423e-196">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="2423e-197">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="2423e-197">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="2423e-198">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="2423e-198">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="2423e-199">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="2423e-199">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="2423e-200">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="2423e-200">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="2423e-201">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2423e-201">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

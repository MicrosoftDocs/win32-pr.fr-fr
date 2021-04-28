---
description: D3DXCreateVolumeTextureFromFileEx fonction-crée une texture de volume à partir d’un fichier.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: D3DXCreateVolumeTextureFromFileEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11be9da24be7fc9a03bab8e761e55a601715bd75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102747"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="2a528-103">D3DXCreateVolumeTextureFromFileEx fonction)</span><span class="sxs-lookup"><span data-stu-id="2a528-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="2a528-104">Crée une texture de volume à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a528-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a528-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2a528-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a528-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2a528-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2a528-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="2a528-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-112">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2a528-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2a528-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2a528-114">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2a528-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2a528-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="2a528-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-116">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-118">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="2a528-118">Width in pixels.</span></span> <span data-ttu-id="2a528-119">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2a528-120">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2a528-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2a528-121">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-123">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2a528-123">Height, in pixels.</span></span> <span data-ttu-id="2a528-124">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2a528-125">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2a528-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2a528-126">*Profondeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-128">Profondeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2a528-128">Depth, in pixels.</span></span> <span data-ttu-id="2a528-129">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2a528-130">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="2a528-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2a528-131">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-133">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="2a528-133">Number of mip levels requested.</span></span> <span data-ttu-id="2a528-134">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="2a528-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-135">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-136">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-137">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="2a528-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2a528-138">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="2a528-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2a528-139">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="2a528-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="2a528-140">Si D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2a528-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2a528-141">D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="2a528-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="2a528-142">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="2a528-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a528-143">*Format*</span><span class="sxs-lookup"><span data-stu-id="2a528-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="2a528-144">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2a528-145">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="2a528-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="2a528-146">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="2a528-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2a528-147">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="2a528-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="2a528-148">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="2a528-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="2a528-149">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a528-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-150">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-151">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2a528-152">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="2a528-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-153">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-154">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-155">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="2a528-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2a528-156">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a528-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-157">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-158">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a528-159">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="2a528-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2a528-160">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="2a528-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="2a528-161">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="2a528-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-162">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a528-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-163">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2a528-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2a528-164">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="2a528-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2a528-165">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="2a528-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2a528-166">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="2a528-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2a528-167">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="2a528-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-168">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a528-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-169">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a528-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2a528-170">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="2a528-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-171">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2a528-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-172">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="2a528-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2a528-173">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="2a528-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a528-174">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2a528-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a528-175">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2a528-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="2a528-176">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="2a528-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a528-177">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a528-177">Return value</span></span>

<span data-ttu-id="2a528-178">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a528-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a528-179">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a528-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2a528-180">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2a528-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a528-181">Notes </span><span class="sxs-lookup"><span data-stu-id="2a528-181">Remarks</span></span>

<span data-ttu-id="2a528-182">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2a528-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2a528-183">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="2a528-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="2a528-184">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromFileExA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="2a528-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="2a528-185">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="2a528-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2a528-186">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2a528-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2a528-187">Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture de volume chargée.</span><span class="sxs-lookup"><span data-stu-id="2a528-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="2a528-188">Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="2a528-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="2a528-189">Dans ce cas, les images doivent être chargées manuellement.</span><span class="sxs-lookup"><span data-stu-id="2a528-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="2a528-190">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="2a528-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="2a528-191">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="2a528-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a528-192">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a528-192">Requirements</span></span>



| <span data-ttu-id="2a528-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a528-193">Requirement</span></span> | <span data-ttu-id="2a528-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a528-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a528-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a528-195">Header</span></span><br/>  | <dl> <span data-ttu-id="2a528-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a528-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2a528-197">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a528-197">Library</span></span><br/> | <dl> <span data-ttu-id="2a528-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a528-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2a528-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a528-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a528-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="2a528-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="2a528-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="2a528-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="2a528-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="2a528-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="2a528-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="2a528-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="2a528-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="2a528-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="2a528-205">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2a528-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

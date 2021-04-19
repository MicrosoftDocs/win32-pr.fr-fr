---
description: Crée une texture de cube à partir d’un fichier. Il s’agit d’une fonction plus avancée que D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: D3DXCreateCubeTextureFromFileEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527131"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="1fe97-104">D3DXCreateCubeTextureFromFileEx fonction)</span><span class="sxs-lookup"><span data-stu-id="1fe97-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="1fe97-105">Crée une texture de cube à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="1fe97-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="1fe97-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="1fe97-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe97-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fe97-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="1fe97-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fe97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe97-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1fe97-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="1fe97-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-112">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-113">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-114">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1fe97-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="1fe97-115">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1fe97-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1fe97-116">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1fe97-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="1fe97-117">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1fe97-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-118">*Taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-120">Largeur et hauteur de la texture du cube, en pixels.</span><span class="sxs-lookup"><span data-stu-id="1fe97-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="1fe97-121">Par exemple, si la texture du cube est un cube de 8 pixels par 8 pixels, la valeur de ce paramètre doit être 8.</span><span class="sxs-lookup"><span data-stu-id="1fe97-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="1fe97-122">Si cette valeur est 0 ou D3DX \_ default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="1fe97-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-123">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-125">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="1fe97-125">Number of mip levels requested.</span></span> <span data-ttu-id="1fe97-126">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="1fe97-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-127">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-129">0 ou D3DUSAGE \_ RENDERTARGET, ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="1fe97-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="1fe97-130">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1fe97-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="1fe97-131">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1fe97-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="1fe97-132">Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="1fe97-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="1fe97-133">D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="1fe97-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="1fe97-134">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="1fe97-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-135">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-136">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="1fe97-137">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="1fe97-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="1fe97-138">La texture de cube retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="1fe97-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="1fe97-139">Les applications doivent vérifier le format de la texture de cube retournée.</span><span class="sxs-lookup"><span data-stu-id="1fe97-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="1fe97-140">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="1fe97-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="1fe97-141">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1fe97-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-142">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-143">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="1fe97-144">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture de cube doit être placée.</span><span class="sxs-lookup"><span data-stu-id="1fe97-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-145">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-146">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-147">Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) , contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="1fe97-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="1fe97-148">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1fe97-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-149">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-150">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fe97-151">Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="1fe97-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="1fe97-152">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="1fe97-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="1fe97-153">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="1fe97-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-154">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-155">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="1fe97-156">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="1fe97-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="1fe97-157">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="1fe97-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="1fe97-158">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="1fe97-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="1fe97-159">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="1fe97-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-160">*pSrcInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-161">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fe97-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="1fe97-162">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1fe97-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-163">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-164">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="1fe97-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1fe97-165">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1fe97-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1fe97-166">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1fe97-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe97-167">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="1fe97-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="1fe97-168">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="1fe97-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe97-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fe97-169">Return value</span></span>

<span data-ttu-id="1fe97-170">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fe97-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fe97-171">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fe97-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1fe97-172">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1fe97-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe97-173">Notes</span><span class="sxs-lookup"><span data-stu-id="1fe97-173">Remarks</span></span>

<span data-ttu-id="1fe97-174">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="1fe97-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1fe97-175">Si Unicode est défini, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileExW**.</span><span class="sxs-lookup"><span data-stu-id="1fe97-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="1fe97-176">Dans le cas contraire, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileExA** , car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="1fe97-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="1fe97-177">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="1fe97-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="1fe97-178">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="1fe97-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="1fe97-179">Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces.</span><span class="sxs-lookup"><span data-stu-id="1fe97-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="1fe97-180">Pour appeler [**SetRenderTarget**](/windows/desktop/api) avec une texture de cube, vous devez sélectionner un visage individuel à l’aide de [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) et passer la surface résultante à **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="1fe97-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="1fe97-181">**D3DXCreateCubeTextureFromFileEx** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="1fe97-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="1fe97-182">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="1fe97-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="1fe97-183">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="1fe97-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="1fe97-184">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="1fe97-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="1fe97-185">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter.</span><span class="sxs-lookup"><span data-stu-id="1fe97-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="1fe97-186">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.</span><span class="sxs-lookup"><span data-stu-id="1fe97-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe97-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fe97-187">Requirements</span></span>



| <span data-ttu-id="1fe97-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fe97-188">Requirement</span></span> | <span data-ttu-id="1fe97-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fe97-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe97-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fe97-190">Header</span></span><br/>  | <dl> <span data-ttu-id="1fe97-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe97-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1fe97-192">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fe97-192">Library</span></span><br/> | <dl> <span data-ttu-id="1fe97-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fe97-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1fe97-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fe97-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe97-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="1fe97-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="1fe97-196">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1fe97-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

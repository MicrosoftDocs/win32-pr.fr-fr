---
description: Crée une texture à partir d’une ressource. Il s’agit d’une fonction plus avancée que D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: D3DXCreateTextureFromResourceEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530915"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="fdb6e-104">D3DXCreateTextureFromResourceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="fdb6e-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="fdb6e-105">Crée une texture à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-105">Creates a texture from a resource.</span></span> <span data-ttu-id="fdb6e-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="fdb6e-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb6e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdb6e-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="fdb6e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fdb6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb6e-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fdb6e-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-113">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-114">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-115">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-116">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-117">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="fdb6e-118">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fdb6e-119">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fdb6e-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-121">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-123">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-123">Width in pixels.</span></span> <span data-ttu-id="fdb6e-124">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-125">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-127">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-127">Height, in pixels.</span></span> <span data-ttu-id="fdb6e-128">Si cette valeur est égale à zéro ou \_ à D3DX default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-129">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-131">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-131">Number of mip levels requested.</span></span> <span data-ttu-id="fdb6e-132">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-133">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-135">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="fdb6e-136">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="fdb6e-137">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fdb6e-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="fdb6e-138">Si D3DUSAGE \_ RENDERTARGET ou D3DUSAGE est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="fdb6e-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="fdb6e-139">D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="fdb6e-140">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [optimisation des performances (Direct3D 9)](performance-optimizations.md)à l’aide de textures dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-141">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-142">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="fdb6e-143">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="fdb6e-144">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="fdb6e-145">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="fdb6e-146">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="fdb6e-147">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-148">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-149">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="fdb6e-150">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-151">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-152">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-153">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="fdb6e-154">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fdb6e-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-155">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-156">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb6e-157">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="fdb6e-158">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="fdb6e-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-159">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-160">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="fdb6e-161">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="fdb6e-162">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="fdb6e-163">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="fdb6e-164">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-165">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-166">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb6e-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="fdb6e-167">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-168">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-169">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="fdb6e-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fdb6e-170">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir ou **null**.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fdb6e-171">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fdb6e-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb6e-172">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="fdb6e-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="fdb6e-173">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb6e-174">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fdb6e-174">Return value</span></span>

<span data-ttu-id="fdb6e-175">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fdb6e-176">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fdb6e-177">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb6e-178">Notes</span><span class="sxs-lookup"><span data-stu-id="fdb6e-178">Remarks</span></span>

<span data-ttu-id="fdb6e-179">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fdb6e-180">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="fdb6e-181">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromResourceExA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="fdb6e-182">La ressource en cours de chargement doit être de type RT \_ bitmap ou RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="fdb6e-183">Le type de ressource « RT \_ RCDATA » est utilisé pour charger des formats autres que des bitmaps (tels que. TGA,. jpg et. DDS).</span><span class="sxs-lookup"><span data-stu-id="fdb6e-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="fdb6e-184">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="fdb6e-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="fdb6e-185">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="fdb6e-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb6e-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdb6e-186">Requirements</span></span>



| <span data-ttu-id="fdb6e-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdb6e-187">Requirement</span></span> | <span data-ttu-id="fdb6e-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdb6e-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb6e-189">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdb6e-189">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb6e-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb6e-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb6e-191">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fdb6e-191">Library</span></span><br/> | <dl> <span data-ttu-id="fdb6e-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb6e-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fdb6e-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdb6e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb6e-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="fdb6e-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="fdb6e-195">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fdb6e-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

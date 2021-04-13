---
description: Crée une texture de cube à partir d’une ressource spécifiée par une chaîne. Il s’agit d’une fonction plus avancée que D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: D3DXCreateCubeTextureFromResourceEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323246"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="7f75c-104">D3DXCreateCubeTextureFromResourceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="7f75c-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="7f75c-105">Crée une texture de cube à partir d’une ressource spécifiée par une chaîne.</span><span class="sxs-lookup"><span data-stu-id="7f75c-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="7f75c-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="7f75c-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f75c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f75c-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="7f75c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f75c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f75c-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7f75c-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="7f75c-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-113">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-114">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="7f75c-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-115">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-116">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-117">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7f75c-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="7f75c-118">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7f75c-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7f75c-119">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7f75c-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7f75c-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7f75c-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-121">*Taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-123">Largeur et hauteur de la texture du cube, en pixels.</span><span class="sxs-lookup"><span data-stu-id="7f75c-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="7f75c-124">Par exemple, si la texture du cube est un cube de 8 pixels par 8 pixels, la valeur de ce paramètre doit être 8.</span><span class="sxs-lookup"><span data-stu-id="7f75c-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="7f75c-125">Si cette valeur est 0 ou D3DX \_ default, les dimensions sont extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="7f75c-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-126">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-127">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-128">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="7f75c-128">Number of mip levels requested.</span></span> <span data-ttu-id="7f75c-129">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="7f75c-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-130">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-132">0 ou D3DUSAGE \_ RENDERTARGET, ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="7f75c-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="7f75c-133">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="7f75c-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="7f75c-134">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="7f75c-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="7f75c-135">Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="7f75c-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="7f75c-136">D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="7f75c-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="7f75c-137">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="7f75c-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-138">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-139">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="7f75c-140">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="7f75c-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="7f75c-141">La texture de cube retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="7f75c-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="7f75c-142">Les applications doivent vérifier le format de la texture de cube retournée.</span><span class="sxs-lookup"><span data-stu-id="7f75c-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="7f75c-143">Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="7f75c-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="7f75c-144">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f75c-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-145">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-146">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="7f75c-147">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture de cube doit être placée.</span><span class="sxs-lookup"><span data-stu-id="7f75c-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-148">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-149">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-150">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md), qui contrôle la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="7f75c-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="7f75c-151">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7f75c-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-152">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-153">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f75c-154">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="7f75c-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7f75c-155">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="7f75c-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-156">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-157">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7f75c-158">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="7f75c-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7f75c-159">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="7f75c-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7f75c-160">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="7f75c-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7f75c-161">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="7f75c-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-162">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-163">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f75c-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="7f75c-164">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="7f75c-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-165">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-166">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="7f75c-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7f75c-167">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir ou **null**.</span><span class="sxs-lookup"><span data-stu-id="7f75c-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f75c-168">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f75c-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f75c-169">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7f75c-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="7f75c-170">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="7f75c-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f75c-171">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f75c-171">Return value</span></span>

<span data-ttu-id="7f75c-172">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f75c-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f75c-173">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f75c-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7f75c-174">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7f75c-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f75c-175">Notes</span><span class="sxs-lookup"><span data-stu-id="7f75c-175">Remarks</span></span>

<span data-ttu-id="7f75c-176">Le paramètre du compilateur détermine la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7f75c-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="7f75c-177">Si Unicode est défini, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromResourceExW**.</span><span class="sxs-lookup"><span data-stu-id="7f75c-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="7f75c-178">Dans le cas contraire, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromResourceExA** , car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="7f75c-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="7f75c-179">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="7f75c-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7f75c-180">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7f75c-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7f75c-181">Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces.</span><span class="sxs-lookup"><span data-stu-id="7f75c-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="7f75c-182">Pour appeler [**SetRenderTarget**](/windows/desktop/api) avec une texture de cube, vous devez sélectionner un visage individuel à l’aide de [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) et passer la surface résultante à **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="7f75c-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="7f75c-183">**D3DXCreateCubeTextureFromResourceEx** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="7f75c-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="7f75c-184">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="7f75c-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="7f75c-185">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="7f75c-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="7f75c-186">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="7f75c-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f75c-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f75c-187">Requirements</span></span>



| <span data-ttu-id="7f75c-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f75c-188">Requirement</span></span> | <span data-ttu-id="7f75c-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f75c-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f75c-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f75c-190">Header</span></span><br/>  | <dl> <span data-ttu-id="7f75c-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f75c-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7f75c-192">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f75c-192">Library</span></span><br/> | <dl> <span data-ttu-id="7f75c-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f75c-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7f75c-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f75c-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f75c-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="7f75c-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="7f75c-196">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7f75c-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

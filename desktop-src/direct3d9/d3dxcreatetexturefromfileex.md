---
description: Crée une texture à partir d’un fichier. Il s’agit d’une fonction plus avancée que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: D3DXCreateTextureFromFileEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870105"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="a733a-104">D3DXCreateTextureFromFileEx fonction)</span><span class="sxs-lookup"><span data-stu-id="a733a-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="a733a-105">Crée une texture à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="a733a-105">Creates a texture from a file.</span></span> <span data-ttu-id="a733a-106">Il s’agit d’une fonction plus avancée que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="a733a-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a733a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a733a-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="a733a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a733a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a733a-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a733a-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a733a-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="a733a-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-112">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-113">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-114">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="a733a-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="a733a-115">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a733a-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a733a-116">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a733a-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="a733a-117">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a733a-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-118">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-120">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="a733a-120">Width in pixels.</span></span> <span data-ttu-id="a733a-121">Si cette valeur est égale à zéro ou D3DX \_ par défaut, les dimensions sont extraites du fichier et arrondies à une puissance de deux.</span><span class="sxs-lookup"><span data-stu-id="a733a-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="a733a-122">Si l’appareil prend en charge les textures non-puissance de 2 et que la [ \_ valeur par défaut de D3DX \_ NONPOW2](other-d3dx-constants.md) est spécifiée, la taille n’est pas arrondie.</span><span class="sxs-lookup"><span data-stu-id="a733a-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-123">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-124">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-125">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="a733a-125">Height, in pixels.</span></span> <span data-ttu-id="a733a-126">Si cette valeur est égale à zéro ou D3DX \_ par défaut, les dimensions sont extraites du fichier et arrondies à une puissance de deux.</span><span class="sxs-lookup"><span data-stu-id="a733a-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="a733a-127">Si l’appareil prend en charge les textures non-puissance de 2 et que la [ \_ valeur par défaut de D3DX \_ NONPOW2](other-d3dx-constants.md) est sepcified, la taille n’est pas arrondie.</span><span class="sxs-lookup"><span data-stu-id="a733a-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-128">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-130">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="a733a-130">Number of mip levels requested.</span></span> <span data-ttu-id="a733a-131">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="a733a-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="a733a-132">Si D3DX \_ à partir d' \_ un fichier, la taille est prise exactement telle qu’elle figure dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a733a-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-133">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-135">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ dynamique**.</span><span class="sxs-lookup"><span data-stu-id="a733a-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="a733a-136">L’affectation de la valeur **D3DUSAGE \_ RENDERTARGET** à cet indicateur indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="a733a-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="a733a-137">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a733a-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a733a-138">Si **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="a733a-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="a733a-139">**D3DUSAGE \_ DYNAMIQUE** indique que l’aire de conception doit être gérée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="a733a-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="a733a-140">Consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="a733a-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="a733a-141">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-142">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="a733a-143">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="a733a-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="a733a-144">La texture retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="a733a-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="a733a-145">Les applications doivent vérifier le format de la texture retournée.</span><span class="sxs-lookup"><span data-stu-id="a733a-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="a733a-146">Si D3DFMT \_ est inconnu, le format est extrait du fichier.</span><span class="sxs-lookup"><span data-stu-id="a733a-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="a733a-147">Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a733a-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-148">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-149">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="a733a-150">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="a733a-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-151">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-152">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-153">Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="a733a-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="a733a-154">La spécification de la [ \_ valeur D3DX par défaut](other-d3dx-constants.md) pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a733a-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-155">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-156">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a733a-157">Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="a733a-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="a733a-158">La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a733a-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="a733a-159">En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.</span><span class="sxs-lookup"><span data-stu-id="a733a-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-160">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a733a-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-161">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a733a-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a733a-162">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver la clé de couleur.</span><span class="sxs-lookup"><span data-stu-id="a733a-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="a733a-163">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="a733a-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a733a-164">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="a733a-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a733a-165">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="a733a-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-166">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a733a-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-167">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a733a-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a733a-168">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a733a-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-169">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a733a-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-170">Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="a733a-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a733a-171">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a733a-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a733a-172">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a733a-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a733a-173">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="a733a-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="a733a-174">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="a733a-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a733a-175">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a733a-175">Return value</span></span>

<span data-ttu-id="a733a-176">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a733a-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a733a-177">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a733a-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a733a-178">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a733a-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a733a-179">Notes</span><span class="sxs-lookup"><span data-stu-id="a733a-179">Remarks</span></span>

<span data-ttu-id="a733a-180">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a733a-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="a733a-181">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="a733a-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="a733a-182">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromFileExA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="a733a-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="a733a-183">Utilisez [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) pour déterminer si votre appareil peut prendre en charge la texture en fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="a733a-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="a733a-184">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="a733a-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a733a-185">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="a733a-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a733a-186">Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="a733a-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="a733a-187">Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="a733a-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="a733a-188">Dans ce cas, les images doivent être chargées manuellement.</span><span class="sxs-lookup"><span data-stu-id="a733a-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="a733a-189">Pour des performances optimales lors de l’utilisation de **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="a733a-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="a733a-190">La mise à l’échelle des images et la conversion du format au moment du chargement peuvent être lentes.</span><span class="sxs-lookup"><span data-stu-id="a733a-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="a733a-191">Stockez les images au format et à la résolution qu’elles seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="a733a-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="a733a-192">Si le matériel cible requiert des dimensions de puissance de 2, créez et stockez des images en utilisant des dimensions de puissance de 2.</span><span class="sxs-lookup"><span data-stu-id="a733a-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="a733a-193">Pour la création d’image mipmap au moment du chargement, filtrez à l’aide de [ \_ \_ la zone de filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a733a-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="a733a-194">Un filtre de zone est beaucoup plus rapide que les autres types de filtres tels que le \_ triangle de filtre D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a733a-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="a733a-195">Envisagez d’utiliser des fichiers DDS.</span><span class="sxs-lookup"><span data-stu-id="a733a-195">Consider using DDS files.</span></span> <span data-ttu-id="a733a-196">Étant donné que les fichiers DDS peuvent être utilisés pour représenter n’importe quel format de texture Direct3D 9, ils sont très faciles à lire pour D3DX.</span><span class="sxs-lookup"><span data-stu-id="a733a-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="a733a-197">En outre, ils peuvent stocker des des mipmaps, de sorte que tous les algorithmes de génération de mipmap peuvent être utilisés pour créer les images.</span><span class="sxs-lookup"><span data-stu-id="a733a-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="a733a-198">En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter.</span><span class="sxs-lookup"><span data-stu-id="a733a-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="a733a-199">Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.</span><span class="sxs-lookup"><span data-stu-id="a733a-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a733a-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a733a-200">Requirements</span></span>



| <span data-ttu-id="a733a-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a733a-201">Requirement</span></span> | <span data-ttu-id="a733a-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="a733a-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a733a-203">En-tête</span><span class="sxs-lookup"><span data-stu-id="a733a-203">Header</span></span><br/>  | <dl> <span data-ttu-id="a733a-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a733a-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a733a-205">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a733a-205">Library</span></span><br/> | <dl> <span data-ttu-id="a733a-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a733a-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a733a-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a733a-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a733a-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="a733a-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="a733a-209">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a733a-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

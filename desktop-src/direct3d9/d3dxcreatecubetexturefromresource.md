---
description: Crée une texture de cube à partir d’une ressource.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: D3DXCreateCubeTextureFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531552"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="809e7-103">D3DXCreateCubeTextureFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="809e7-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="809e7-104">Crée une texture de cube à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="809e7-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="809e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="809e7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="809e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="809e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="809e7-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="809e7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="809e7-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="809e7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="809e7-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="809e7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="809e7-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="809e7-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="809e7-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="809e7-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="809e7-112">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="809e7-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="809e7-113">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="809e7-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="809e7-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="809e7-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="809e7-115">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="809e7-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="809e7-116">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="809e7-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="809e7-117">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="809e7-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="809e7-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="809e7-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="809e7-119">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="809e7-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="809e7-120">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="809e7-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="809e7-121">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="809e7-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="809e7-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="809e7-122">Return value</span></span>

<span data-ttu-id="809e7-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="809e7-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="809e7-124">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="809e7-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="809e7-125">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="809e7-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="809e7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="809e7-126">Remarks</span></span>

<span data-ttu-id="809e7-127">Le paramètre du compilateur détermine la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="809e7-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="809e7-128">Si Unicode est défini, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="809e7-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="809e7-129">Dans le cas contraire, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromResourceA** , car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="809e7-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="809e7-130">La fonction est équivalente à D3DXCreateCubeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="809e7-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="809e7-131">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="809e7-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="809e7-132">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="809e7-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="809e7-133">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="809e7-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="809e7-134">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="809e7-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="809e7-135">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="809e7-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="809e7-136">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="809e7-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="809e7-137">**D3DXCreateCubeTextureFromResource** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="809e7-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="809e7-138">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="809e7-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="809e7-139">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="809e7-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="809e7-140">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="809e7-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="809e7-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="809e7-141">Requirements</span></span>



| <span data-ttu-id="809e7-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="809e7-142">Requirement</span></span> | <span data-ttu-id="809e7-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="809e7-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="809e7-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="809e7-144">Header</span></span><br/>  | <dl> <span data-ttu-id="809e7-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="809e7-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="809e7-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="809e7-146">Library</span></span><br/> | <dl> <span data-ttu-id="809e7-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="809e7-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="809e7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="809e7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809e7-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="809e7-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="809e7-150">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="809e7-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

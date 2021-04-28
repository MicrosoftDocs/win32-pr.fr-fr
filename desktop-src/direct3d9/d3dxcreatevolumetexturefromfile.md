---
description: D3DXCreateVolumeTextureFromFile fonction-crée une texture de volume à partir d’un fichier.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: D3DXCreateVolumeTextureFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094299"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="91438-103">D3DXCreateVolumeTextureFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="91438-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="91438-104">Crée une texture de volume à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="91438-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="91438-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91438-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="91438-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91438-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91438-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91438-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91438-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="91438-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="91438-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="91438-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="91438-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91438-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91438-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91438-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91438-112">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="91438-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="91438-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="91438-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="91438-114">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="91438-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="91438-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="91438-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="91438-116">*ppVolumeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91438-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91438-117">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="91438-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="91438-118">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="91438-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91438-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91438-119">Return value</span></span>

<span data-ttu-id="91438-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91438-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91438-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91438-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91438-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="91438-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="91438-123">Notes </span><span class="sxs-lookup"><span data-stu-id="91438-123">Remarks</span></span>

<span data-ttu-id="91438-124">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="91438-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="91438-125">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="91438-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="91438-126">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="91438-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="91438-127">La fonction est équivalente à D3DXCreateVolumeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX par défaut \_ , D3DX default \_ , D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="91438-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="91438-128">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="91438-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="91438-129">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="91438-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="91438-130">Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="91438-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="91438-131">Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="91438-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="91438-132">Dans ce cas, les images doivent être chargées manuellement.</span><span class="sxs-lookup"><span data-stu-id="91438-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="91438-133">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="91438-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="91438-134">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="91438-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="91438-135">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="91438-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="91438-136">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="91438-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91438-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91438-137">Requirements</span></span>



| <span data-ttu-id="91438-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91438-138">Requirement</span></span> | <span data-ttu-id="91438-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="91438-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91438-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="91438-140">Header</span></span><br/>  | <dl> <span data-ttu-id="91438-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="91438-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="91438-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91438-142">Library</span></span><br/> | <dl> <span data-ttu-id="91438-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91438-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="91438-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91438-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91438-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="91438-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="91438-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="91438-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="91438-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="91438-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="91438-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="91438-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="91438-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="91438-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="91438-150">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="91438-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

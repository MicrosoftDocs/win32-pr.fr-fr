---
description: Crée une texture de volume à partir d’une ressource.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: D3DXCreateVolumeTextureFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530909"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="6cc55-103">D3DXCreateVolumeTextureFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="6cc55-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="6cc55-104">Crée une texture de volume à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="6cc55-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc55-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cc55-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6cc55-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cc55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc55-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cc55-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc55-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6cc55-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6cc55-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="6cc55-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6cc55-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cc55-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc55-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc55-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6cc55-112">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="6cc55-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="6cc55-113">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cc55-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc55-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc55-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6cc55-115">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6cc55-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="6cc55-116">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6cc55-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6cc55-117">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6cc55-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6cc55-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6cc55-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6cc55-119">*ppVolumeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cc55-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc55-120">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6cc55-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="6cc55-121">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="6cc55-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc55-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cc55-122">Return value</span></span>

<span data-ttu-id="6cc55-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6cc55-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6cc55-124">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6cc55-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6cc55-125">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6cc55-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc55-126">Notes</span><span class="sxs-lookup"><span data-stu-id="6cc55-126">Remarks</span></span>

<span data-ttu-id="6cc55-127">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6cc55-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6cc55-128">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="6cc55-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="6cc55-129">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateVolumeTextureFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="6cc55-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="6cc55-130">La fonction est équivalente à D3DXCreateVolumeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX par défaut, \_ D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="6cc55-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="6cc55-131">La ressource en cours de chargement doit être une ressource définie par l’application (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="6cc55-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="6cc55-132">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="6cc55-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="6cc55-133">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="6cc55-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="6cc55-134">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="6cc55-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="6cc55-135">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="6cc55-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="6cc55-136">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6cc55-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="6cc55-137">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="6cc55-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc55-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cc55-138">Requirements</span></span>



| <span data-ttu-id="6cc55-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cc55-139">Requirement</span></span> | <span data-ttu-id="6cc55-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc55-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc55-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cc55-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6cc55-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc55-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6cc55-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cc55-143">Library</span></span><br/> | <dl> <span data-ttu-id="6cc55-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cc55-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6cc55-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cc55-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc55-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="6cc55-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="6cc55-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="6cc55-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="6cc55-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6cc55-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6cc55-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="6cc55-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="6cc55-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="6cc55-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="6cc55-151">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6cc55-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Crée une texture de volume à partir d’un fichier en mémoire.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: D3DXCreateVolumeTextureFromFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762061"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a><span data-ttu-id="111ea-103">D3DXCreateVolumeTextureFromFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="111ea-103">D3DXCreateVolumeTextureFromFileInMemory function</span></span>

<span data-ttu-id="111ea-104">Crée une texture de volume à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="111ea-104">Creates a volume texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="111ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="111ea-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="111ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="111ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="111ea-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="111ea-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111ea-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="111ea-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="111ea-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="111ea-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="111ea-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="111ea-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111ea-111">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="111ea-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="111ea-112">Pointeur vers le fichier en mémoire à partir duquel créer la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="111ea-112">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="111ea-113">*SrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="111ea-113">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111ea-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="111ea-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="111ea-115">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="111ea-115">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="111ea-116">*ppVolumeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="111ea-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="111ea-117">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="111ea-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="111ea-118">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="111ea-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="111ea-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="111ea-119">Return value</span></span>

<span data-ttu-id="111ea-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="111ea-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="111ea-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="111ea-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="111ea-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="111ea-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="111ea-123">Notes</span><span class="sxs-lookup"><span data-stu-id="111ea-123">Remarks</span></span>

<span data-ttu-id="111ea-124">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="111ea-124">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="111ea-125">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="111ea-125">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="111ea-126">La fonction est équivalente à D3DXCreateVolumeTextureFromFileInMemoryEx (pDevice, pSrcFile, SrcData, D3DX \_ default, D3DX par défaut, \_ D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="111ea-126">The function is equivalent to D3DXCreateVolumeTextureFromFileInMemoryEx(pDevice, pSrcFile, SrcData, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="111ea-127">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="111ea-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="111ea-128">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="111ea-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="111ea-129">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="111ea-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="111ea-130">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="111ea-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="111ea-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="111ea-131">Requirements</span></span>



| <span data-ttu-id="111ea-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="111ea-132">Requirement</span></span> | <span data-ttu-id="111ea-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="111ea-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="111ea-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="111ea-134">Header</span></span><br/>  | <dl> <span data-ttu-id="111ea-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="111ea-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="111ea-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="111ea-136">Library</span></span><br/> | <dl> <span data-ttu-id="111ea-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="111ea-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="111ea-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="111ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111ea-139">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="111ea-139">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="111ea-140">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="111ea-140">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="111ea-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="111ea-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="111ea-142">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="111ea-142">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="111ea-143">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="111ea-143">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="111ea-144">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="111ea-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

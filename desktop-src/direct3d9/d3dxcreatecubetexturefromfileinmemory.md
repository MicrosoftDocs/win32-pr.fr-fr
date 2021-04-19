---
description: Crée une texture de cube à partir d’un fichier en mémoire.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: D3DXCreateCubeTextureFromFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106541253"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="760e2-103">D3DXCreateCubeTextureFromFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="760e2-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="760e2-104">Crée une texture de cube à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="760e2-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="760e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="760e2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="760e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760e2-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="760e2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="760e2-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="760e2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="760e2-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="760e2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="760e2-110">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="760e2-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="760e2-111">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="760e2-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="760e2-112">Pointeur vers le fichier en mémoire à partir duquel créer le carte cubique.</span><span class="sxs-lookup"><span data-stu-id="760e2-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="760e2-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="760e2-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="760e2-114">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="760e2-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="760e2-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="760e2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="760e2-116">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="760e2-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="760e2-117">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="760e2-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="760e2-118">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="760e2-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="760e2-119">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="760e2-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760e2-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="760e2-120">Return value</span></span>

<span data-ttu-id="760e2-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="760e2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="760e2-122">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="760e2-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="760e2-123">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="760e2-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="760e2-124">Notes</span><span class="sxs-lookup"><span data-stu-id="760e2-124">Remarks</span></span>

<span data-ttu-id="760e2-125">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="760e2-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="760e2-126">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="760e2-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="760e2-127">La fonction est équivalente à D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="760e2-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="760e2-128">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="760e2-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="760e2-129">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="760e2-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="760e2-130">Cette méthode est conçue pour être utilisée pour charger des fichiers image stockés en tant que RT \_ RCDATA, qui est une ressource définie par l’application (données brutes).</span><span class="sxs-lookup"><span data-stu-id="760e2-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="760e2-131">Dans le cas contraire, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="760e2-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="760e2-132">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="760e2-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="760e2-133">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="760e2-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="760e2-134">**D3DXCreateCubeTextureFromFileInMemory** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="760e2-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="760e2-135">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="760e2-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="760e2-136">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="760e2-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="760e2-137">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="760e2-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="760e2-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="760e2-138">Requirements</span></span>



| <span data-ttu-id="760e2-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="760e2-139">Requirement</span></span> | <span data-ttu-id="760e2-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="760e2-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="760e2-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="760e2-141">Header</span></span><br/>  | <dl> <span data-ttu-id="760e2-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="760e2-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="760e2-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="760e2-143">Library</span></span><br/> | <dl> <span data-ttu-id="760e2-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="760e2-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="760e2-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="760e2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760e2-146">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="760e2-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

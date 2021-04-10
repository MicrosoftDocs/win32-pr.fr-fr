---
description: Crée une texture à partir d’un fichier en mémoire.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: D3DXCreateTextureFromFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762067"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="ca992-103">D3DXCreateTextureFromFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="ca992-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="ca992-104">Crée une texture à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ca992-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca992-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca992-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ca992-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca992-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca992-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca992-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ca992-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ca992-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="ca992-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ca992-110">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca992-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca992-111">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca992-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca992-112">Pointeur vers le fichier en mémoire à partir duquel créer la texture.</span><span class="sxs-lookup"><span data-stu-id="ca992-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ca992-113">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca992-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca992-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca992-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca992-115">Taille en octets du fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ca992-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca992-116">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ca992-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca992-117">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ca992-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="ca992-118">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="ca992-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca992-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca992-119">Return value</span></span>

<span data-ttu-id="ca992-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca992-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca992-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca992-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca992-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ca992-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca992-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ca992-123">Remarks</span></span>

<span data-ttu-id="ca992-124">La fonction est équivalente à D3DXCreateTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, D3DX par défaut \_ , D3DX \_ default, 0, D3DFMT \_ UNknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="ca992-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="ca992-125">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="ca992-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ca992-126">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ca992-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ca992-127">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="ca992-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="ca992-128">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="ca992-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="ca992-129">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ca992-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="ca992-130">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ca992-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca992-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca992-131">Requirements</span></span>



| <span data-ttu-id="ca992-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca992-132">Requirement</span></span> | <span data-ttu-id="ca992-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca992-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca992-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca992-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ca992-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca992-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ca992-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca992-136">Library</span></span><br/> | <dl> <span data-ttu-id="ca992-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca992-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ca992-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca992-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca992-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ca992-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="ca992-140">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ca992-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Enregistre une texture dans un fichier image.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: D3DXSaveTextureToFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116214"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="3871e-103">D3DXSaveTextureToFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="3871e-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="3871e-104">Enregistre une texture dans un fichier image.</span><span class="sxs-lookup"><span data-stu-id="3871e-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3871e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3871e-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="3871e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3871e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3871e-107">*ppDestBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3871e-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3871e-108">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3871e-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3871e-109">Adresse d’un pointeur vers un [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’image.</span><span class="sxs-lookup"><span data-stu-id="3871e-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="3871e-110">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3871e-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3871e-111">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3871e-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="3871e-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3871e-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="3871e-113">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="3871e-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="3871e-114">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3871e-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3871e-115">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="3871e-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="3871e-116">Pointeur vers l’interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) contenant l’image à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="3871e-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="3871e-117">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3871e-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3871e-118">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="3871e-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="3871e-119">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="3871e-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="3871e-120">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3871e-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3871e-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3871e-121">Return value</span></span>

<span data-ttu-id="3871e-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3871e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3871e-123">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3871e-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3871e-124">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3871e-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3871e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3871e-125">Remarks</span></span>

<span data-ttu-id="3871e-126">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="3871e-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="3871e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3871e-127">Requirements</span></span>



| <span data-ttu-id="3871e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3871e-128">Requirement</span></span> | <span data-ttu-id="3871e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3871e-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3871e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3871e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3871e-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3871e-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3871e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3871e-132">Library</span></span><br/> | <dl> <span data-ttu-id="3871e-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3871e-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3871e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3871e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3871e-135">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="3871e-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="3871e-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3871e-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="3871e-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3871e-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 

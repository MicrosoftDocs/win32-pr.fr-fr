---
description: Enregistre une surface dans un fichier image.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: D3DXSaveSurfaceToFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538330"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="1477e-103">D3DXSaveSurfaceToFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="1477e-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="1477e-104">Enregistre une surface dans un fichier image.</span><span class="sxs-lookup"><span data-stu-id="1477e-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1477e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1477e-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="1477e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1477e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1477e-107">*ppDestBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1477e-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1477e-108">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1477e-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1477e-109">Adresse d’un pointeur vers un [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’image.</span><span class="sxs-lookup"><span data-stu-id="1477e-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="1477e-110">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1477e-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1477e-111">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1477e-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="1477e-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1477e-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="1477e-113">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="1477e-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="1477e-114">*pSrcSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1477e-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1477e-115">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="1477e-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="1477e-116">Pointeur vers l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) contenant l’image à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="1477e-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="1477e-117">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1477e-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1477e-118">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1477e-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1477e-119">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="1477e-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="1477e-120">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1477e-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1477e-121">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1477e-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1477e-122">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="1477e-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="1477e-123">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1477e-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="1477e-124">Spécifie le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="1477e-124">Specifies the source rectangle.</span></span> <span data-ttu-id="1477e-125">Affectez la valeur **null** à ce paramètre pour spécifier la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="1477e-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1477e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1477e-126">Return value</span></span>

<span data-ttu-id="1477e-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1477e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1477e-128">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1477e-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1477e-129">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1477e-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1477e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1477e-130">Remarks</span></span>

<span data-ttu-id="1477e-131">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="1477e-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="1477e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1477e-132">Requirements</span></span>



| <span data-ttu-id="1477e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1477e-133">Requirement</span></span> | <span data-ttu-id="1477e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1477e-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1477e-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1477e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1477e-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1477e-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1477e-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1477e-137">Library</span></span><br/> | <dl> <span data-ttu-id="1477e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1477e-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1477e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1477e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1477e-140">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1477e-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="1477e-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="1477e-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 

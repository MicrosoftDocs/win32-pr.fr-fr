---
description: Enregistre un volume dans une mémoire tampon. La méthode crée une mémoire tampon ID3DXBuffer pour stocker les données et retourne cet objet.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: D3DXSaveVolumeToFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211745"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="fcabe-104">D3DXSaveVolumeToFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="fcabe-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="fcabe-105">Enregistre un volume dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fcabe-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="fcabe-106">La méthode crée une mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) pour stocker les données et retourne cet objet.</span><span class="sxs-lookup"><span data-stu-id="fcabe-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcabe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcabe-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="fcabe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcabe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcabe-109">*ppDestBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fcabe-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-110">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcabe-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fcabe-111">Adresse d’un pointeur vers une mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’image.</span><span class="sxs-lookup"><span data-stu-id="fcabe-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="fcabe-112">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcabe-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-113">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="fcabe-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="fcabe-114">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fcabe-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="fcabe-115">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="fcabe-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="fcabe-116">*pSrcVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcabe-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-117">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="fcabe-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="fcabe-118">Pointeur vers l’interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) contenant l’image à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fcabe-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fcabe-119">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcabe-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-120">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fcabe-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fcabe-121">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="fcabe-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="fcabe-122">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fcabe-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fcabe-123">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcabe-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-124">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcabe-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="fcabe-125">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="fcabe-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="fcabe-126">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="fcabe-126">Specifies the source box.</span></span> <span data-ttu-id="fcabe-127">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="fcabe-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcabe-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcabe-128">Return value</span></span>

<span data-ttu-id="fcabe-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcabe-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcabe-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fcabe-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcabe-131">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="fcabe-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="fcabe-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcabe-132">Requirements</span></span>



| <span data-ttu-id="fcabe-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcabe-133">Requirement</span></span> | <span data-ttu-id="fcabe-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcabe-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcabe-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcabe-135">Header</span></span><br/>  | <dl> <span data-ttu-id="fcabe-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcabe-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fcabe-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcabe-137">Library</span></span><br/> | <dl> <span data-ttu-id="fcabe-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcabe-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fcabe-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcabe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcabe-140">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fcabe-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="fcabe-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="fcabe-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 

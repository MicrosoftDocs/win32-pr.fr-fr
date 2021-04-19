---
description: Enregistre une surface dans un fichier.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: D3DXSaveSurfaceToFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543770"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="fe57e-103">D3DXSaveSurfaceToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="fe57e-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="fe57e-104">Enregistre une surface dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="fe57e-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe57e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe57e-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="fe57e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe57e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe57e-107">*pDestFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe57e-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57e-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe57e-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe57e-109">Pointeur vers une chaîne qui spécifie le nom de fichier de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="fe57e-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="fe57e-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fe57e-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fe57e-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fe57e-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fe57e-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fe57e-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fe57e-113">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe57e-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57e-114">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="fe57e-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="fe57e-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fe57e-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="fe57e-116">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="fe57e-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="fe57e-117">*pSrcSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe57e-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57e-118">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="fe57e-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="fe57e-119">Pointeur vers l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , contenant l’image à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fe57e-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fe57e-120">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe57e-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57e-121">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fe57e-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fe57e-122">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="fe57e-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="fe57e-123">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe57e-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe57e-124">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe57e-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57e-125">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="fe57e-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="fe57e-126">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe57e-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="fe57e-127">Spécifie le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="fe57e-127">Specifies the source rectangle.</span></span> <span data-ttu-id="fe57e-128">Affectez la valeur **null** à ce paramètre pour spécifier la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="fe57e-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe57e-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe57e-129">Return value</span></span>

<span data-ttu-id="fe57e-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe57e-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe57e-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe57e-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe57e-132">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="fe57e-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="fe57e-133">Notes</span><span class="sxs-lookup"><span data-stu-id="fe57e-133">Remarks</span></span>

<span data-ttu-id="fe57e-134">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe57e-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fe57e-135">Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveSurfaceToFileW.</span><span class="sxs-lookup"><span data-stu-id="fe57e-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="fe57e-136">Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveSurfaceToFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="fe57e-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="fe57e-137">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="fe57e-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe57e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe57e-138">Requirements</span></span>



| <span data-ttu-id="fe57e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe57e-139">Requirement</span></span> | <span data-ttu-id="fe57e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe57e-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe57e-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe57e-141">Header</span></span><br/>  | <dl> <span data-ttu-id="fe57e-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe57e-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fe57e-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe57e-143">Library</span></span><br/> | <dl> <span data-ttu-id="fe57e-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe57e-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fe57e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe57e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe57e-146">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fe57e-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="fe57e-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="fe57e-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="fe57e-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="fe57e-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 

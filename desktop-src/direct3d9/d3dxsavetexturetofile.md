---
description: Enregistre une texture dans un fichier.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: D3DXSaveTextureToFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529607"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="5de92-103">D3DXSaveTextureToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="5de92-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="5de92-104">Enregistre une texture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5de92-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5de92-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="5de92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5de92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de92-107">*pDestFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5de92-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de92-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5de92-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5de92-109">Pointeur vers une chaîne qui spécifie le nom de fichier de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="5de92-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="5de92-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5de92-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5de92-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5de92-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5de92-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5de92-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5de92-113">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5de92-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de92-114">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5de92-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="5de92-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5de92-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="5de92-116">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="5de92-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="5de92-117">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5de92-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de92-118">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="5de92-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="5de92-119">Pointeur vers l’interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , contenant la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5de92-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="5de92-120">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5de92-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de92-121">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="5de92-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5de92-122">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="5de92-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="5de92-123">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5de92-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de92-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5de92-124">Return value</span></span>

<span data-ttu-id="5de92-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5de92-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5de92-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5de92-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5de92-127">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="5de92-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="5de92-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5de92-128">Remarks</span></span>

<span data-ttu-id="5de92-129">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5de92-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5de92-130">Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveTextureToFileW.</span><span class="sxs-lookup"><span data-stu-id="5de92-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="5de92-131">Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveTextureToFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="5de92-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="5de92-132">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="5de92-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="5de92-133">Si le volume n’est pas dynamique (en raison d’un paramètre d’utilisation défini à 0 lors de la création) et situé dans la mémoire vidéo (le pool de mémoire défini sur D3DPOOL \_ par défaut), **D3DXSaveTextureToFile** échoue car D3DX ne peut pas verrouiller les volumes non dynamiques situés dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="5de92-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="5de92-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5de92-134">Requirements</span></span>



| <span data-ttu-id="5de92-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5de92-135">Requirement</span></span> | <span data-ttu-id="5de92-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5de92-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5de92-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="5de92-137">Header</span></span><br/>  | <dl> <span data-ttu-id="5de92-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de92-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5de92-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5de92-139">Library</span></span><br/> | <dl> <span data-ttu-id="5de92-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de92-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5de92-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5de92-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de92-142">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5de92-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="5de92-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="5de92-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="5de92-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="5de92-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 

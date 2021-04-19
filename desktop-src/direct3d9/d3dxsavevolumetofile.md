---
description: Enregistre un volume dans un fichier sur le disque.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: D3DXSaveVolumeToFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527101"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="229b0-103">D3DXSaveVolumeToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="229b0-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="229b0-104">Enregistre un volume dans un fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="229b0-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="229b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="229b0-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="229b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="229b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229b0-107">*pDestFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="229b0-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229b0-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="229b0-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="229b0-109">Pointeur vers une chaîne qui spécifie le nom de fichier de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="229b0-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="229b0-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="229b0-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="229b0-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="229b0-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="229b0-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="229b0-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="229b0-113">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="229b0-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229b0-114">Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="229b0-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="229b0-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="229b0-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="229b0-116">Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="229b0-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="229b0-117">*pSrcVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="229b0-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229b0-118">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="229b0-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="229b0-119">Pointeur vers l’interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) contenant l’image à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="229b0-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="229b0-120">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="229b0-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229b0-121">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="229b0-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="229b0-122">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="229b0-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="229b0-123">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="229b0-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="229b0-124">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="229b0-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229b0-125">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="229b0-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="229b0-126">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="229b0-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="229b0-127">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="229b0-127">Specifies the source box.</span></span> <span data-ttu-id="229b0-128">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="229b0-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="229b0-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="229b0-129">Return value</span></span>

<span data-ttu-id="229b0-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="229b0-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="229b0-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="229b0-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="229b0-132">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="229b0-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="229b0-133">Notes</span><span class="sxs-lookup"><span data-stu-id="229b0-133">Remarks</span></span>

<span data-ttu-id="229b0-134">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="229b0-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="229b0-135">Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveVolumeToFileW.</span><span class="sxs-lookup"><span data-stu-id="229b0-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="229b0-136">Dans le cas contraire, l’appel de fonction est résolu en >D3DXSaveVolumeToFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="229b0-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="229b0-137">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="229b0-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="229b0-138">Si le volume n’est pas dynamique (en raison d’un paramètre d’utilisation défini à 0 lors de la création) et situé dans la mémoire vidéo (le pool de mémoire défini sur D3DPOOL \_ par défaut), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) échoue car D3DX ne peut pas verrouiller les volumes non dynamiques situés dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="229b0-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="229b0-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="229b0-139">Requirements</span></span>



| <span data-ttu-id="229b0-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="229b0-140">Requirement</span></span> | <span data-ttu-id="229b0-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="229b0-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="229b0-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="229b0-142">Header</span></span><br/>  | <dl> <span data-ttu-id="229b0-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="229b0-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="229b0-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="229b0-144">Library</span></span><br/> | <dl> <span data-ttu-id="229b0-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="229b0-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="229b0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="229b0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229b0-147">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="229b0-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="229b0-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="229b0-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="229b0-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="229b0-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="229b0-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="229b0-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 

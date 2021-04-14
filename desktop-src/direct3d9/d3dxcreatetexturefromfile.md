---
description: Crée une texture à partir d’un fichier.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: D3DXCreateTextureFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394128"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="908f3-103">D3DXCreateTextureFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="908f3-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="908f3-104">Crée une texture à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="908f3-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="908f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="908f3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="908f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="908f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908f3-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="908f3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="908f3-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="908f3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="908f3-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="908f3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="908f3-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="908f3-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="908f3-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="908f3-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="908f3-112">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="908f3-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="908f3-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="908f3-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="908f3-114">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="908f3-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="908f3-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="908f3-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="908f3-116">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="908f3-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="908f3-117">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="908f3-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="908f3-118">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="908f3-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908f3-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="908f3-119">Return value</span></span>

<span data-ttu-id="908f3-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="908f3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="908f3-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="908f3-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="908f3-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="908f3-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="908f3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="908f3-123">Remarks</span></span>

<span data-ttu-id="908f3-124">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="908f3-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="908f3-125">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="908f3-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="908f3-126">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="908f3-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="908f3-127">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="908f3-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="908f3-128">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="908f3-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="908f3-129">La fonction est équivalente à D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ par défaut, D3DX default, \_ 0, D3DFMT \_ UNknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null,** ppTexture).</span><span class="sxs-lookup"><span data-stu-id="908f3-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="908f3-130">Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="908f3-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="908f3-131">Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="908f3-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="908f3-132">Dans ce cas, les images doivent être chargées manuellement.</span><span class="sxs-lookup"><span data-stu-id="908f3-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="908f3-133">Notez qu’une ressource créée avec cette fonction sera placée dans la classe de mémoire indiquée par D3DPOOL \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="908f3-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="908f3-134">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="908f3-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="908f3-135">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="908f3-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="908f3-136">Pour des performances optimales lors de l’utilisation de **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="908f3-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="908f3-137">La mise à l’échelle des images et la conversion du format au moment du chargement peuvent être lentes.</span><span class="sxs-lookup"><span data-stu-id="908f3-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="908f3-138">Stockez les images au format et à la résolution qu’elles seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="908f3-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="908f3-139">Si le matériel cible requiert une puissance de deux dimensions, créez et stockez des images à l’aide de la puissance de deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="908f3-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="908f3-140">Envisagez d’utiliser des fichiers de surface DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="908f3-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="908f3-141">Étant donné que les fichiers DDS peuvent être utilisés pour représenter n’importe quel format de texture Direct3D 9, ils sont très faciles à lire pour D3DX.</span><span class="sxs-lookup"><span data-stu-id="908f3-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="908f3-142">En outre, ils peuvent stocker des des mipmaps, de sorte que tous les algorithmes de génération de mipmap peuvent être utilisés pour créer les images.</span><span class="sxs-lookup"><span data-stu-id="908f3-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="908f3-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="908f3-143">Requirements</span></span>



| <span data-ttu-id="908f3-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="908f3-144">Requirement</span></span> | <span data-ttu-id="908f3-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="908f3-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="908f3-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="908f3-146">Header</span></span><br/>  | <dl> <span data-ttu-id="908f3-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="908f3-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="908f3-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="908f3-148">Library</span></span><br/> | <dl> <span data-ttu-id="908f3-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="908f3-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="908f3-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="908f3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908f3-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="908f3-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="908f3-152">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="908f3-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

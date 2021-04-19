---
description: Crée une texture de cube à partir d’un fichier.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: D3DXCreateCubeTextureFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522360"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="0a69d-103">D3DXCreateCubeTextureFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="0a69d-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="0a69d-104">Crée une texture de cube à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0a69d-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a69d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a69d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="0a69d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a69d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a69d-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a69d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a69d-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0a69d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0a69d-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="0a69d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="0a69d-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a69d-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a69d-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a69d-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a69d-112">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a69d-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="0a69d-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0a69d-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0a69d-114">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0a69d-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0a69d-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0a69d-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0a69d-116">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a69d-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a69d-117">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="0a69d-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="0a69d-118">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="0a69d-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a69d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a69d-119">Return value</span></span>

<span data-ttu-id="0a69d-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a69d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a69d-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a69d-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a69d-122">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0a69d-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a69d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0a69d-123">Remarks</span></span>

<span data-ttu-id="0a69d-124">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="0a69d-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0a69d-125">Si Unicode est défini, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileW**.</span><span class="sxs-lookup"><span data-stu-id="0a69d-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="0a69d-126">Dans le cas contraire, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileA** , car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="0a69d-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="0a69d-127">La fonction est équivalente à D3DXCreateCubeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="0a69d-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="0a69d-128">Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="0a69d-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="0a69d-129">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="0a69d-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="0a69d-130">Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée.</span><span class="sxs-lookup"><span data-stu-id="0a69d-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="0a69d-131">Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="0a69d-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="0a69d-132">Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0a69d-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="0a69d-133">Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0a69d-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="0a69d-134">**D3DXCreateCubeTextureFromFile** utilise le format de fichier de la surface DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="0a69d-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="0a69d-135">L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="0a69d-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="0a69d-136">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="0a69d-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="0a69d-137">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="0a69d-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a69d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a69d-138">Requirements</span></span>



| <span data-ttu-id="0a69d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a69d-139">Requirement</span></span> | <span data-ttu-id="0a69d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a69d-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a69d-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a69d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0a69d-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a69d-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0a69d-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a69d-143">Library</span></span><br/> | <dl> <span data-ttu-id="0a69d-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a69d-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0a69d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a69d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a69d-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="0a69d-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="0a69d-147">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0a69d-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

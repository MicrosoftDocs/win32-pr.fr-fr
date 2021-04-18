---
description: Crée une texture de cube vide, en ajustant les paramètres d’appel en fonction des besoins.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: D3DXCreateCubeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527132"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="19287-103">D3DXCreateCubeTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="19287-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="19287-104">Crée une texture de cube vide, en ajustant les paramètres d’appel en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="19287-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="19287-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19287-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="19287-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19287-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="19287-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="19287-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="19287-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="19287-110">*Taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19287-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19287-112">Largeur et hauteur de la texture du cube, en pixels.</span><span class="sxs-lookup"><span data-stu-id="19287-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="19287-113">Par exemple, si la texture du cube est un cube de 8 pixels par 8 pixels, la valeur de ce paramètre doit être 8.</span><span class="sxs-lookup"><span data-stu-id="19287-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="19287-114">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19287-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19287-116">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="19287-116">Number of mip levels requested.</span></span> <span data-ttu-id="19287-117">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="19287-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="19287-118">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-119">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19287-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19287-120">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="19287-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="19287-121">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="19287-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="19287-122">La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="19287-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="19287-123">Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="19287-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="19287-124">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="19287-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="19287-125">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-126">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="19287-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="19287-127">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du cube.</span><span class="sxs-lookup"><span data-stu-id="19287-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="19287-128">La texture de cube retournée peut avoir un format différent de celui spécifié par le *format*.</span><span class="sxs-lookup"><span data-stu-id="19287-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="19287-129">Les applications doivent vérifier le format de la texture de cube retournée.</span><span class="sxs-lookup"><span data-stu-id="19287-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="19287-130">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19287-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-131">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="19287-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="19287-132">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture de cube doit être placée.</span><span class="sxs-lookup"><span data-stu-id="19287-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="19287-133">*ppCubeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19287-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19287-134">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="19287-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="19287-135">Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.</span><span class="sxs-lookup"><span data-stu-id="19287-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19287-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19287-136">Return value</span></span>

<span data-ttu-id="19287-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19287-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19287-138">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19287-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19287-139">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19287-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19287-140">Notes</span><span class="sxs-lookup"><span data-stu-id="19287-140">Remarks</span></span>

<span data-ttu-id="19287-141">Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces.</span><span class="sxs-lookup"><span data-stu-id="19287-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="19287-142">En interne, D3DXCreateCubeTexture utilise [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) pour ajuster les paramètres d’appel.</span><span class="sxs-lookup"><span data-stu-id="19287-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="19287-143">Par conséquent, les appels à D3DXCreateCubeTexture aboutissent souvent lorsque les appels à [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) échouent.</span><span class="sxs-lookup"><span data-stu-id="19287-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="19287-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19287-144">Requirements</span></span>



| <span data-ttu-id="19287-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19287-145">Requirement</span></span> | <span data-ttu-id="19287-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="19287-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19287-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="19287-147">Header</span></span><br/>  | <dl> <span data-ttu-id="19287-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="19287-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="19287-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19287-149">Library</span></span><br/> | <dl> <span data-ttu-id="19287-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19287-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="19287-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19287-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19287-152">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="19287-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

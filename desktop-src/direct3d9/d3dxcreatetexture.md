---
description: Crée une texture vide, en ajustant les paramètres d’appel en fonction des besoins.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: D3DXCreateTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530916"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="44d12-103">D3DXCreateTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="44d12-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="44d12-104">Crée une texture vide, en ajustant les paramètres d’appel en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="44d12-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d12-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44d12-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="44d12-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44d12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d12-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="44d12-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="44d12-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="44d12-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-110">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d12-112">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="44d12-112">Width in pixels.</span></span> <span data-ttu-id="44d12-113">Si cette valeur est égale à 0, la valeur 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="44d12-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="44d12-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="44d12-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-115">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d12-117">Hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="44d12-117">Height in pixels.</span></span> <span data-ttu-id="44d12-118">Si cette valeur est égale à 0, la valeur 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="44d12-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="44d12-119">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="44d12-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-120">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d12-122">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="44d12-122">Number of mip levels requested.</span></span> <span data-ttu-id="44d12-123">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="44d12-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-124">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d12-126">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ dynamique**.</span><span class="sxs-lookup"><span data-stu-id="44d12-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="44d12-127">L’affectation de la valeur **D3DUSAGE \_ RENDERTARGET** à cet indicateur indique que la surface doit être utilisée comme cible de rendu en appelant la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="44d12-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="44d12-128">Si **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="44d12-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="44d12-129">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="44d12-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="44d12-130">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-131">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="44d12-132">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture.</span><span class="sxs-lookup"><span data-stu-id="44d12-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="44d12-133">La texture retournée peut être d’un format différent de celui spécifié, si l’appareil ne prend pas en charge le format demandé.</span><span class="sxs-lookup"><span data-stu-id="44d12-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="44d12-134">Les applications doivent vérifier le format de la texture retournée pour voir si elle correspond au format demandé.</span><span class="sxs-lookup"><span data-stu-id="44d12-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-135">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44d12-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-136">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="44d12-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="44d12-137">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="44d12-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="44d12-138">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="44d12-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44d12-139">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="44d12-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="44d12-140">Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="44d12-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d12-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44d12-141">Return value</span></span>

<span data-ttu-id="44d12-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44d12-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44d12-143">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44d12-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="44d12-144">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="44d12-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d12-145">Notes</span><span class="sxs-lookup"><span data-stu-id="44d12-145">Remarks</span></span>

<span data-ttu-id="44d12-146">En interne, D3DXCreateTexture utilise [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) pour ajuster les paramètres d’appel.</span><span class="sxs-lookup"><span data-stu-id="44d12-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="44d12-147">Par conséquent, les appels à D3DXCreateTexture aboutissent souvent lorsque les appels à [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) échouent.</span><span class="sxs-lookup"><span data-stu-id="44d12-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="44d12-148">Si la hauteur et la largeur sont définies sur [D3DX \_ default](other-d3dx-constants.md), la valeur 256 est utilisée pour les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="44d12-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="44d12-149">Si la hauteur ou la largeur est définie sur D3DX \_ Default et que l’autre paramètre est défini sur une valeur numérique, la texture sera carré avec la hauteur et la largeur égales à la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="44d12-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d12-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44d12-150">Requirements</span></span>



| <span data-ttu-id="44d12-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44d12-151">Requirement</span></span> | <span data-ttu-id="44d12-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="44d12-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44d12-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="44d12-153">Header</span></span><br/>  | <dl> <span data-ttu-id="44d12-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d12-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="44d12-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="44d12-155">Library</span></span><br/> | <dl> <span data-ttu-id="44d12-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44d12-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="44d12-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44d12-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d12-158">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="44d12-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

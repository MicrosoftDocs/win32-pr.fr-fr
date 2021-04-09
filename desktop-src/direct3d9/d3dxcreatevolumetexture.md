---
description: Crée une texture de volume vide, en ajustant les paramètres d’appel en fonction des besoins.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: D3DXCreateVolumeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953855"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="ae110-103">D3DXCreateVolumeTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="ae110-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="ae110-104">Crée une texture de volume vide, en ajustant les paramètres d’appel en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="ae110-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae110-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae110-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ae110-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae110-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae110-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ae110-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ae110-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="ae110-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ae110-110">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae110-112">Largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="ae110-112">Width in pixels.</span></span> <span data-ttu-id="ae110-113">Cette valeur doit être différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ae110-113">This value must be nonzero.</span></span> <span data-ttu-id="ae110-114">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ae110-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ae110-115">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae110-117">Hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="ae110-117">Height in pixels.</span></span> <span data-ttu-id="ae110-118">Cette valeur doit être différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ae110-118">This value must be nonzero.</span></span> <span data-ttu-id="ae110-119">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ae110-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ae110-120">*Profondeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae110-122">Profondeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="ae110-122">Depth in pixels.</span></span> <span data-ttu-id="ae110-123">Cette valeur doit être différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ae110-123">This value must be nonzero.</span></span> <span data-ttu-id="ae110-124">La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ae110-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ae110-125">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae110-127">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="ae110-127">Number of mip levels requested.</span></span> <span data-ttu-id="ae110-128">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="ae110-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ae110-129">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae110-131">0 ou D3DUSAGE \_ dynamique.</span><span class="sxs-lookup"><span data-stu-id="ae110-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ae110-132">Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ae110-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae110-133">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-134">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ae110-135">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="ae110-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="ae110-136">La texture de volume retournée peut avoir un format différent de celui spécifié par le format.</span><span class="sxs-lookup"><span data-stu-id="ae110-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="ae110-137">Les applications doivent vérifier le format de la texture de volume retournée.</span><span class="sxs-lookup"><span data-stu-id="ae110-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ae110-138">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae110-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-139">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ae110-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ae110-140">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture du volume doit être placée.</span><span class="sxs-lookup"><span data-stu-id="ae110-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ae110-141">*ppVolumeTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae110-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae110-142">Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ae110-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ae110-143">Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , représentant l’objet de texture de volume créé.</span><span class="sxs-lookup"><span data-stu-id="ae110-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae110-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae110-144">Return value</span></span>

<span data-ttu-id="ae110-145">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae110-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae110-146">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae110-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae110-147">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ae110-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="ae110-148">Notes</span><span class="sxs-lookup"><span data-stu-id="ae110-148">Remarks</span></span>

<span data-ttu-id="ae110-149">En interne, D3DXCreateVolumeTexture utilise [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) pour ajuster les paramètres d’appel.</span><span class="sxs-lookup"><span data-stu-id="ae110-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="ae110-150">Par conséquent, les appels à D3DXCreateVolumeTexture aboutissent souvent lorsque les appels à [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) échouent.</span><span class="sxs-lookup"><span data-stu-id="ae110-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae110-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae110-151">Requirements</span></span>



| <span data-ttu-id="ae110-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae110-152">Requirement</span></span> | <span data-ttu-id="ae110-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae110-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae110-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae110-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ae110-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae110-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ae110-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae110-156">Library</span></span><br/> | <dl> <span data-ttu-id="ae110-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae110-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae110-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae110-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae110-159">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ae110-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

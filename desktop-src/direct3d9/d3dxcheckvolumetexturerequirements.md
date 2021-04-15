---
description: Vérifie les paramètres de création de texture de volume.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: D3DXCheckVolumeTextureRequirements, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394152"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="d60da-103">D3DXCheckVolumeTextureRequirements fonction)</span><span class="sxs-lookup"><span data-stu-id="d60da-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="d60da-104">Vérifie les paramètres de création de texture de volume.</span><span class="sxs-lookup"><span data-stu-id="d60da-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d60da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d60da-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="d60da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d60da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d60da-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d60da-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d60da-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d60da-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="d60da-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d60da-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d60da-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d60da-112">Pointeur vers la largeur demandée en pixels, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d60da-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="d60da-113">Retourne la taille corrigée.</span><span class="sxs-lookup"><span data-stu-id="d60da-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d60da-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-115">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d60da-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d60da-116">Pointeur vers la hauteur demandée en pixels, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d60da-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="d60da-117">Retourne la taille corrigée.</span><span class="sxs-lookup"><span data-stu-id="d60da-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-118">*pDepth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d60da-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-119">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d60da-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d60da-120">Pointeur vers la profondeur demandée en pixels, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d60da-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="d60da-121">Retourne la taille corrigée.</span><span class="sxs-lookup"><span data-stu-id="d60da-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-122">*pNumMipLevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d60da-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-123">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d60da-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d60da-124">Pointeur vers le nombre de niveaux de mipmap demandés, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d60da-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="d60da-125">Retourne le nombre corrigé de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d60da-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-126">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d60da-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d60da-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d60da-128">Actuellement non utilisé, affectez la valeur 0 à.</span><span class="sxs-lookup"><span data-stu-id="d60da-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-129">*pFormat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d60da-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-130">Type : **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="d60da-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="d60da-131">Pointeur vers un membre du type énuméré [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d60da-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="d60da-132">Spécifie le format de pixel souhaité, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d60da-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="d60da-133">Retourne le format corrigé.</span><span class="sxs-lookup"><span data-stu-id="d60da-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="d60da-134">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d60da-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d60da-135">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d60da-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="d60da-136">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture du volume doit être placée.</span><span class="sxs-lookup"><span data-stu-id="d60da-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d60da-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d60da-137">Return value</span></span>

<span data-ttu-id="d60da-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d60da-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d60da-139">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d60da-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d60da-140">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d60da-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d60da-141">Notes</span><span class="sxs-lookup"><span data-stu-id="d60da-141">Remarks</span></span>

<span data-ttu-id="d60da-142">Si les paramètres de cette fonction ne sont pas valides, cette fonction retourne les paramètres corrigés.</span><span class="sxs-lookup"><span data-stu-id="d60da-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60da-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d60da-143">Requirements</span></span>



| <span data-ttu-id="d60da-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d60da-144">Requirement</span></span> | <span data-ttu-id="d60da-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d60da-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d60da-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="d60da-146">Header</span></span><br/>  | <dl> <span data-ttu-id="d60da-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d60da-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d60da-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d60da-148">Library</span></span><br/> | <dl> <span data-ttu-id="d60da-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d60da-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d60da-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d60da-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60da-151">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d60da-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

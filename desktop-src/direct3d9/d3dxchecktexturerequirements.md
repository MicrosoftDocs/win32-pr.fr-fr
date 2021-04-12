---
description: Vérifie les paramètres de création de texture.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: D3DXCheckTextureRequirements, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211806"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="e585f-103">D3DXCheckTextureRequirements fonction)</span><span class="sxs-lookup"><span data-stu-id="e585f-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="e585f-104">Vérifie les paramètres de création de texture.</span><span class="sxs-lookup"><span data-stu-id="e585f-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e585f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e585f-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="e585f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e585f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e585f-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e585f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e585f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e585f-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.</span><span class="sxs-lookup"><span data-stu-id="e585f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e585f-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e585f-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e585f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e585f-112">Pointeur vers la largeur demandée en pixels, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e585f-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="e585f-113">Retourne la taille corrigée.</span><span class="sxs-lookup"><span data-stu-id="e585f-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e585f-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e585f-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-115">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e585f-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e585f-116">Pointeur vers la hauteur demandée en pixels, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e585f-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="e585f-117">Retourne la taille corrigée.</span><span class="sxs-lookup"><span data-stu-id="e585f-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e585f-118">*pNumMipLevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e585f-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-119">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e585f-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e585f-120">Pointeur vers le nombre de niveaux de mipmap demandés, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e585f-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="e585f-121">Retourne le nombre corrigé de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="e585f-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="e585f-122">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e585f-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e585f-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e585f-124">0 ou [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="e585f-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="e585f-125">L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e585f-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e585f-126">La ressource peut ensuite être transmise au paramètre pNewRenderTarget de la méthode [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e585f-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e585f-127">Si **D3DUSAGE \_ RENDERTARGET** est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="e585f-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="e585f-128">*pFormat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e585f-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-129">Type : **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="e585f-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="e585f-130">Pointeur vers un membre du type énuméré [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="e585f-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="e585f-131">Spécifie le format de pixel souhaité, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e585f-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="e585f-132">Retourne le format corrigé.</span><span class="sxs-lookup"><span data-stu-id="e585f-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="e585f-133">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e585f-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e585f-134">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e585f-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e585f-135">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.</span><span class="sxs-lookup"><span data-stu-id="e585f-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e585f-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e585f-136">Return value</span></span>

<span data-ttu-id="e585f-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e585f-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e585f-138">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e585f-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e585f-139">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e585f-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e585f-140">Notes</span><span class="sxs-lookup"><span data-stu-id="e585f-140">Remarks</span></span>

<span data-ttu-id="e585f-141">Si les paramètres de cette fonction ne sont pas valides, cette fonction retourne les paramètres corrigés.</span><span class="sxs-lookup"><span data-stu-id="e585f-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="e585f-142">Cette fonction utilise l’heuristique suivante lors de la comparaison des exigences demandées par rapport aux formats disponibles :</span><span class="sxs-lookup"><span data-stu-id="e585f-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="e585f-143">Ne choisissez pas un format comportant moins de canaux.</span><span class="sxs-lookup"><span data-stu-id="e585f-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="e585f-144">Évitez les formats [FourCC](d3dformat.md) et 24 bits sauf demande explicite.</span><span class="sxs-lookup"><span data-stu-id="e585f-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="e585f-145">Essayez de ne pas ajouter de nouveaux canaux.</span><span class="sxs-lookup"><span data-stu-id="e585f-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="e585f-146">Essayez de ne pas modifier le nombre de bits par canal.</span><span class="sxs-lookup"><span data-stu-id="e585f-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="e585f-147">Essayez d’éviter la conversion entre les types de formats.</span><span class="sxs-lookup"><span data-stu-id="e585f-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="e585f-148">Par exemple, évitez de convertir un format ARVB en un format de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e585f-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="e585f-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e585f-149">Requirements</span></span>



| <span data-ttu-id="e585f-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e585f-150">Requirement</span></span> | <span data-ttu-id="e585f-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="e585f-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e585f-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="e585f-152">Header</span></span><br/>  | <dl> <span data-ttu-id="e585f-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e585f-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e585f-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e585f-154">Library</span></span><br/> | <dl> <span data-ttu-id="e585f-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e585f-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e585f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e585f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e585f-157">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e585f-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

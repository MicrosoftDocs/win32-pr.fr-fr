---
description: Définit une valeur Albedo pour chaque Texel, en remplaçant les valeurs Albedo précédentes.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'ID3DXPRTEngine :: SetPerTexelAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394167"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a><span data-ttu-id="2a98b-103">ID3DXPRTEngine :: SetPerTexelAlbedo, méthode</span><span class="sxs-lookup"><span data-stu-id="2a98b-103">ID3DXPRTEngine::SetPerTexelAlbedo method</span></span>

<span data-ttu-id="2a98b-104">Définit une valeur Albedo pour chaque Texel, en remplaçant les valeurs Albedo précédentes.</span><span class="sxs-lookup"><span data-stu-id="2a98b-104">Sets an albedo value for each texel, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a98b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a98b-105">Syntax</span></span>


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="2a98b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a98b-107">*pAlbedoTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a98b-107">*pAlbedoTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a98b-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="2a98b-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="2a98b-109">Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) dans lequel stocker les valeurs Albedo.</span><span class="sxs-lookup"><span data-stu-id="2a98b-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object in which to store albedo values.</span></span>

</dd> <dt>

<span data-ttu-id="2a98b-110">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a98b-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a98b-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a98b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a98b-112">Nombre de canaux de couleur à définir.</span><span class="sxs-lookup"><span data-stu-id="2a98b-112">Number of color channels to set.</span></span> <span data-ttu-id="2a98b-113">Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="2a98b-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="2a98b-114">*pGH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a98b-114">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a98b-115">Type : **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="2a98b-115">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="2a98b-116">Pointeur facultatif vers un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="2a98b-116">Optional pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object.</span></span> <span data-ttu-id="2a98b-117">S’il n’est pas fourni, un objet d’assistance de la marge de texture est créé et détruit en interne.</span><span class="sxs-lookup"><span data-stu-id="2a98b-117">If not provided, a texture gutter helper object is created and destroyed internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a98b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a98b-118">Return value</span></span>

<span data-ttu-id="2a98b-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a98b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a98b-120">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a98b-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a98b-121">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2a98b-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLED3DERR\_OUTOFVIDEOMEMORY, D3DERR\_WASSTILLDRAWING, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a98b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a98b-122">Requirements</span></span>



| <span data-ttu-id="2a98b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a98b-123">Requirement</span></span> | <span data-ttu-id="2a98b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a98b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a98b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a98b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2a98b-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a98b-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2a98b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a98b-127">Library</span></span><br/> | <dl> <span data-ttu-id="2a98b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a98b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a98b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a98b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a98b-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="2a98b-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 

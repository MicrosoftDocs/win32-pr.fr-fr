---
description: Lancer le rendu d’un mappage d’environnement parabolique.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'ID3DXRenderToEnvMap :: BeginParabolic, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043092"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="db4a1-103">ID3DXRenderToEnvMap :: BeginParabolic, méthode</span><span class="sxs-lookup"><span data-stu-id="db4a1-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="db4a1-104">Lancer le rendu d’un mappage d’environnement parabolique.</span><span class="sxs-lookup"><span data-stu-id="db4a1-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db4a1-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="db4a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db4a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4a1-107">*pTexZPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db4a1-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db4a1-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="db4a1-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="db4a1-109">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture de rendu positive.</span><span class="sxs-lookup"><span data-stu-id="db4a1-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="db4a1-110">*pTexZNeg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db4a1-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db4a1-111">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="db4a1-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="db4a1-112">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture de rendu négative.</span><span class="sxs-lookup"><span data-stu-id="db4a1-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db4a1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db4a1-113">Return value</span></span>

<span data-ttu-id="db4a1-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db4a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db4a1-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db4a1-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db4a1-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. E \_ échec</span><span class="sxs-lookup"><span data-stu-id="db4a1-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="db4a1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="db4a1-117">Remarks</span></span>

<span data-ttu-id="db4a1-118">Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner les visages.</span><span class="sxs-lookup"><span data-stu-id="db4a1-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4a1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db4a1-119">Requirements</span></span>



| <span data-ttu-id="db4a1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db4a1-120">Requirement</span></span> | <span data-ttu-id="db4a1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="db4a1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4a1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="db4a1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="db4a1-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4a1-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="db4a1-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db4a1-124">Library</span></span><br/> | <dl> <span data-ttu-id="db4a1-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db4a1-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db4a1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db4a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4a1-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="db4a1-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="db4a1-128">**ID3DXRenderToEnvMap :: fin**</span><span class="sxs-lookup"><span data-stu-id="db4a1-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 

---
description: Lancer le rendu d’une carte d’environnement sphérique.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap :: BeginSphere, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322805"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="94d20-103">ID3DXRenderToEnvMap :: BeginSphere, méthode</span><span class="sxs-lookup"><span data-stu-id="94d20-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="94d20-104">Lancer le rendu d’une carte d’environnement sphérique.</span><span class="sxs-lookup"><span data-stu-id="94d20-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94d20-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="94d20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d20-107">*ptex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94d20-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d20-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="94d20-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="94d20-109">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture vers laquelle effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="94d20-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d20-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94d20-110">Return value</span></span>

<span data-ttu-id="94d20-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="94d20-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="94d20-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="94d20-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="94d20-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. E \_ échec</span><span class="sxs-lookup"><span data-stu-id="94d20-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="94d20-114">Notes</span><span class="sxs-lookup"><span data-stu-id="94d20-114">Remarks</span></span>

<span data-ttu-id="94d20-115">Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner le visage.</span><span class="sxs-lookup"><span data-stu-id="94d20-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d20-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94d20-116">Requirements</span></span>



| <span data-ttu-id="94d20-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94d20-117">Requirement</span></span> | <span data-ttu-id="94d20-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="94d20-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d20-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="94d20-119">Header</span></span><br/>  | <dl> <span data-ttu-id="94d20-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d20-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="94d20-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94d20-121">Library</span></span><br/> | <dl> <span data-ttu-id="94d20-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94d20-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94d20-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94d20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d20-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="94d20-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="94d20-125">**ID3DXRenderToEnvMap :: fin**</span><span class="sxs-lookup"><span data-stu-id="94d20-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 

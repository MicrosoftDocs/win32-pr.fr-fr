---
description: Lancer le rendu d’une carte d’environnement cubique.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'ID3DXRenderToEnvMap :: BeginCube, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322806"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="580d5-103">ID3DXRenderToEnvMap :: BeginCube, méthode</span><span class="sxs-lookup"><span data-stu-id="580d5-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="580d5-104">Lancer le rendu d’une carte d’environnement cubique.</span><span class="sxs-lookup"><span data-stu-id="580d5-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="580d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="580d5-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="580d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="580d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580d5-107">*pCubeTex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="580d5-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580d5-108">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="580d5-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="580d5-109">Pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) qui représente la texture de cube vers laquelle effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="580d5-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580d5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="580d5-110">Return value</span></span>

<span data-ttu-id="580d5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="580d5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="580d5-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="580d5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="580d5-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="580d5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="580d5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="580d5-114">Remarks</span></span>

<span data-ttu-id="580d5-115">Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner chacun des 6 visages.</span><span class="sxs-lookup"><span data-stu-id="580d5-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="580d5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="580d5-116">Requirements</span></span>



| <span data-ttu-id="580d5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="580d5-117">Requirement</span></span> | <span data-ttu-id="580d5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="580d5-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="580d5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="580d5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="580d5-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="580d5-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="580d5-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="580d5-121">Library</span></span><br/> | <dl> <span data-ttu-id="580d5-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="580d5-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="580d5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="580d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580d5-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="580d5-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="580d5-125">**ID3DXRenderToEnvMap :: fin**</span><span class="sxs-lookup"><span data-stu-id="580d5-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 

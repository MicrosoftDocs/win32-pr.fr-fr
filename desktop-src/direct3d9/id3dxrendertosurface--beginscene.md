---
description: Commence une scène.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface :: BeginScene, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522990"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="d3519-103">ID3DXRenderToSurface :: BeginScene, méthode</span><span class="sxs-lookup"><span data-stu-id="d3519-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="d3519-104">Commence une scène.</span><span class="sxs-lookup"><span data-stu-id="d3519-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3519-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3519-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="d3519-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3519-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3519-107">*pSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3519-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3519-108">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="d3519-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="d3519-109">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , qui représente la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="d3519-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="d3519-110">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3519-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3519-111">Type : **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3519-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="d3519-112">Pointeur vers une structure [**D3DVIEWPORT9**](d3dviewport9.md) , décrivant la fenêtre d’affichage de la scène.</span><span class="sxs-lookup"><span data-stu-id="d3519-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3519-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3519-113">Return value</span></span>

<span data-ttu-id="d3519-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3519-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3519-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3519-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d3519-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ sera déplacé E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d3519-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="d3519-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3519-117">Requirements</span></span>



| <span data-ttu-id="d3519-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3519-118">Requirement</span></span> | <span data-ttu-id="d3519-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3519-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3519-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3519-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d3519-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3519-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d3519-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3519-122">Library</span></span><br/> | <dl> <span data-ttu-id="d3519-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3519-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3519-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3519-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3519-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="d3519-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="d3519-126">**ID3DXRenderToSurface::EndScene**</span><span class="sxs-lookup"><span data-stu-id="d3519-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 

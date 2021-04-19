---
description: Prépare un appareil pour le dessin de lignes.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine :: Begin, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542193"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="a7c47-103">ID3DXLine :: Begin, méthode</span><span class="sxs-lookup"><span data-stu-id="a7c47-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="a7c47-104">Prépare un appareil pour le dessin de lignes.</span><span class="sxs-lookup"><span data-stu-id="a7c47-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7c47-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="a7c47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7c47-106">Parameters</span></span>

<span data-ttu-id="a7c47-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a7c47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7c47-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7c47-108">Return value</span></span>

<span data-ttu-id="a7c47-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7c47-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7c47-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7c47-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7c47-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="a7c47-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7c47-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a7c47-112">Remarks</span></span>

<span data-ttu-id="a7c47-113">L’appel de **ID3DXLine :: Begin** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a7c47-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="a7c47-114">Si elle est appelée en dehors d’une séquence ID3DXLine :: Begin/ID3DXLine :: end, les fonctions de dessin appellent en interne ID3DXLine :: Begin et ID3DXLine :: end.</span><span class="sxs-lookup"><span data-stu-id="a7c47-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="a7c47-115">Pour éviter une surcharge supplémentaire, cette méthode doit être utilisée si plusieurs fonctions de dessin seront appelées successivement.</span><span class="sxs-lookup"><span data-stu-id="a7c47-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="a7c47-116">Cette méthode doit être appelée à partir d’une séquence [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) et [**IDirect3DDevice9 :: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="a7c47-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="a7c47-117">ID3DXLine :: Begin ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="a7c47-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c47-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7c47-118">Requirements</span></span>



| <span data-ttu-id="a7c47-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7c47-119">Requirement</span></span> | <span data-ttu-id="a7c47-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7c47-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c47-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7c47-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a7c47-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c47-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a7c47-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a7c47-123">Library</span></span><br/> | <dl> <span data-ttu-id="a7c47-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7c47-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7c47-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7c47-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c47-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="a7c47-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 

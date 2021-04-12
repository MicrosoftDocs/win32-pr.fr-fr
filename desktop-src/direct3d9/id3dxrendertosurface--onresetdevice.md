---
description: Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: 'ID3DXRenderToSurface :: OnResetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09d8e3d2c7b628d36fee12525e9423059a7bd63a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322853"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a><span data-ttu-id="bb8eb-103">ID3DXRenderToSurface :: OnResetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="bb8eb-103">ID3DXRenderToSurface::OnResetDevice method</span></span>

<span data-ttu-id="bb8eb-104">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb8eb-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="bb8eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb8eb-106">Parameters</span></span>

<span data-ttu-id="bb8eb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb8eb-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb8eb-108">Return value</span></span>

<span data-ttu-id="bb8eb-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb8eb-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb8eb-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bb8eb-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8eb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bb8eb-112">Remarks</span></span>

<span data-ttu-id="bb8eb-113">ID3DXRenderToSurface :: OnResetDevice doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-113">ID3DXRenderToSurface::OnResetDevice should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="bb8eb-114">Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8eb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb8eb-115">Requirements</span></span>



| <span data-ttu-id="bb8eb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb8eb-116">Requirement</span></span> | <span data-ttu-id="bb8eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb8eb-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8eb-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb8eb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bb8eb-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8eb-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bb8eb-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb8eb-120">Library</span></span><br/> | <dl> <span data-ttu-id="bb8eb-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb8eb-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb8eb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb8eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8eb-123">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="bb8eb-123">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 

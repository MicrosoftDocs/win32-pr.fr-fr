---
description: Récupère les paramètres de la surface de rendu.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface :: GetDesc, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211936"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="5cfd1-103">ID3DXRenderToSurface :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="5cfd1-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="5cfd1-104">Récupère les paramètres de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="5cfd1-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfd1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cfd1-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="5cfd1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cfd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfd1-107">*pParameters* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5cfd1-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfd1-108">Type : **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5cfd1-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="5cfd1-109">Pointeur vers une structure [**D3DXRTS \_ desc**](d3dxrts-desc.md) décrivant les paramètres de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="5cfd1-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfd1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5cfd1-110">Return value</span></span>

<span data-ttu-id="5cfd1-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5cfd1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5cfd1-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5cfd1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5cfd1-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5cfd1-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfd1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cfd1-114">Requirements</span></span>



| <span data-ttu-id="5cfd1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cfd1-115">Requirement</span></span> | <span data-ttu-id="5cfd1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cfd1-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfd1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cfd1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5cfd1-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cfd1-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5cfd1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5cfd1-119">Library</span></span><br/> | <dl> <span data-ttu-id="5cfd1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5cfd1-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5cfd1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cfd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfd1-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="5cfd1-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 





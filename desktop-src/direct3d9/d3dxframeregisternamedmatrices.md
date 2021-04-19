---
description: À partir d’une hiérarchie d’images, inscrit toutes les matrices nommées dans le mélangeur d’animation.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: D3DXFrameRegisterNamedMatrices, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525878"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="60d4f-103">D3DXFrameRegisterNamedMatrices fonction)</span><span class="sxs-lookup"><span data-stu-id="60d4f-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="60d4f-104">À partir d’une hiérarchie d’images, inscrit toutes les matrices nommées dans le mélangeur d’animation.</span><span class="sxs-lookup"><span data-stu-id="60d4f-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d4f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60d4f-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="60d4f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60d4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d4f-107">*pFrameRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60d4f-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d4f-108">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="60d4f-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="60d4f-109">Nœud de niveau supérieur dans la hiérarchie d’images.</span><span class="sxs-lookup"><span data-stu-id="60d4f-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="60d4f-110">*pAnimController* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60d4f-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d4f-111">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="60d4f-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="60d4f-112">Pointeur vers l’objet de contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="60d4f-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d4f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60d4f-113">Return value</span></span>

<span data-ttu-id="60d4f-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60d4f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60d4f-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60d4f-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60d4f-116">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="60d4f-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d4f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60d4f-117">Requirements</span></span>



| <span data-ttu-id="60d4f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60d4f-118">Requirement</span></span> | <span data-ttu-id="60d4f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="60d4f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d4f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="60d4f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="60d4f-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="60d4f-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="60d4f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60d4f-122">Library</span></span><br/> | <dl> <span data-ttu-id="60d4f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60d4f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60d4f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60d4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d4f-125">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="60d4f-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 





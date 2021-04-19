---
description: Détruit la sous-arborescence des frames sous la racine, y compris la racine.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: D3DXFrameDestroy, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531539"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="abd90-103">D3DXFrameDestroy fonction)</span><span class="sxs-lookup"><span data-stu-id="abd90-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="abd90-104">Détruit la sous-arborescence des frames sous la racine, y compris la racine.</span><span class="sxs-lookup"><span data-stu-id="abd90-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abd90-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="abd90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abd90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd90-107">*pFrameRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd90-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd90-108">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="abd90-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="abd90-109">Pointeur vers le nœud racine.</span><span class="sxs-lookup"><span data-stu-id="abd90-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="abd90-110">*pAlloc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd90-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd90-111">Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="abd90-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="abd90-112">Interface d’allocation utilisée pour libérer des nœuds de la hiérarchie d’images.</span><span class="sxs-lookup"><span data-stu-id="abd90-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abd90-113">Return value</span></span>

<span data-ttu-id="abd90-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abd90-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abd90-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abd90-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="abd90-116">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="abd90-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd90-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abd90-117">Requirements</span></span>



| <span data-ttu-id="abd90-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abd90-118">Requirement</span></span> | <span data-ttu-id="abd90-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="abd90-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abd90-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="abd90-120">Header</span></span><br/>  | <dl> <span data-ttu-id="abd90-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd90-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="abd90-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abd90-122">Library</span></span><br/> | <dl> <span data-ttu-id="abd90-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abd90-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abd90-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abd90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd90-125">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="abd90-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 





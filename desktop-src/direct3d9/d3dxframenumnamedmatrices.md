---
description: Compte le nombre de frames d’une sous-arborescence qui ont des noms non null.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: D3DXFrameNumNamedMatrices, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953850"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="c5b5f-103">D3DXFrameNumNamedMatrices fonction)</span><span class="sxs-lookup"><span data-stu-id="c5b5f-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="c5b5f-104">Compte le nombre de frames d’une sous-arborescence qui ont des noms non null.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5b5f-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="c5b5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5b5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b5f-107">*pFrameRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5b5f-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b5f-108">Type : **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5b5f-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="c5b5f-109">Pointeur vers le nœud racine de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b5f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5b5f-110">Return value</span></span>

<span data-ttu-id="c5b5f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b5f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5b5f-112">Retourne le nombre de frames.</span><span class="sxs-lookup"><span data-stu-id="c5b5f-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b5f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5b5f-113">Requirements</span></span>



| <span data-ttu-id="c5b5f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5b5f-114">Requirement</span></span> | <span data-ttu-id="c5b5f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5b5f-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b5f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5b5f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c5b5f-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b5f-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c5b5f-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5b5f-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5b5f-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5b5f-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5b5f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b5f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b5f-121">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="c5b5f-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

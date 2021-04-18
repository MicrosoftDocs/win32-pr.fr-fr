---
description: Retourne la longueur d’un Quaternion.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: D3DXQuaternionLength, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394212"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="06ab5-103">D3DXQuaternionLength fonction)</span><span class="sxs-lookup"><span data-stu-id="06ab5-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="06ab5-104">Retourne la longueur d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="06ab5-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ab5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06ab5-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="06ab5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ab5-107">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06ab5-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ab5-108">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="06ab5-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="06ab5-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="06ab5-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ab5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06ab5-110">Return value</span></span>

<span data-ttu-id="06ab5-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06ab5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06ab5-112">Longueur du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="06ab5-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ab5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="06ab5-113">Remarks</span></span>

<span data-ttu-id="06ab5-114">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="06ab5-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ab5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06ab5-115">Requirements</span></span>



| <span data-ttu-id="06ab5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06ab5-116">Requirement</span></span> | <span data-ttu-id="06ab5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="06ab5-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06ab5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="06ab5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="06ab5-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ab5-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="06ab5-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06ab5-120">Library</span></span><br/> | <dl> <span data-ttu-id="06ab5-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06ab5-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06ab5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06ab5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ab5-123">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="06ab5-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="06ab5-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="06ab5-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 

---
description: Retourne le carré de la longueur d’un Quaternion.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: D3DXQuaternionLengthSq, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523218"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="880de-103">D3DXQuaternionLengthSq fonction)</span><span class="sxs-lookup"><span data-stu-id="880de-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="880de-104">Retourne le carré de la longueur d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="880de-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="880de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="880de-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="880de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="880de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880de-107">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="880de-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880de-108">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="880de-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="880de-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="880de-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880de-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="880de-110">Return value</span></span>

<span data-ttu-id="880de-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="880de-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="880de-112">Longueur au carré du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="880de-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="880de-113">Notes</span><span class="sxs-lookup"><span data-stu-id="880de-113">Remarks</span></span>

<span data-ttu-id="880de-114">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="880de-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="880de-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880de-115">Requirements</span></span>



| <span data-ttu-id="880de-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="880de-116">Requirement</span></span> | <span data-ttu-id="880de-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="880de-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="880de-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="880de-118">Header</span></span><br/>  | <dl> <span data-ttu-id="880de-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="880de-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="880de-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="880de-120">Library</span></span><br/> | <dl> <span data-ttu-id="880de-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="880de-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="880de-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="880de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880de-123">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="880de-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="880de-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="880de-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 

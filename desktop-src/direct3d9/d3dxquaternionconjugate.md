---
description: Retourne le conjugué d’un Quaternion.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: D3DXQuaternionConjugate, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211848"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="62be9-103">D3DXQuaternionConjugate fonction)</span><span class="sxs-lookup"><span data-stu-id="62be9-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="62be9-104">Retourne le conjugué d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="62be9-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="62be9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62be9-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="62be9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62be9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62be9-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62be9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62be9-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="62be9-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="62be9-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="62be9-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="62be9-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62be9-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62be9-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="62be9-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="62be9-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="62be9-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62be9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62be9-113">Return value</span></span>

<span data-ttu-id="62be9-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="62be9-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="62be9-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le conjugué du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="62be9-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="62be9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="62be9-116">Remarks</span></span>

<span data-ttu-id="62be9-117">À partir d’un Quaternion (x, y, z, w), la fonction **D3DXQuaternionConjugate** retourne le Quaternion (-x,-y,-z, w).</span><span class="sxs-lookup"><span data-stu-id="62be9-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="62be9-118">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="62be9-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="62be9-119">De cette façon, la fonction **D3DXQuaternionConjugate** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="62be9-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="62be9-120">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="62be9-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="62be9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62be9-121">Requirements</span></span>



| <span data-ttu-id="62be9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62be9-122">Requirement</span></span> | <span data-ttu-id="62be9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="62be9-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62be9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="62be9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="62be9-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="62be9-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="62be9-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62be9-126">Library</span></span><br/> | <dl> <span data-ttu-id="62be9-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62be9-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62be9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62be9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62be9-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="62be9-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="62be9-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="62be9-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 





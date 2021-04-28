---
description: 'D3DXMatrixRotationQuaternion, fonction (D3DX10Math. h) : génère une matrice de rotation à partir d’un Quaternion.'
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: D3DXMatrixRotationQuaternion, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103427"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="331e4-103">D3DXMatrixRotationQuaternion, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="331e4-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="331e4-104">Génère une matrice de rotation à partir d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="331e4-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="331e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="331e4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="331e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="331e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="331e4-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="331e4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="331e4-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="331e4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="331e4-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="331e4-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="331e4-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="331e4-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="331e4-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="331e4-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="331e4-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="331e4-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="331e4-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="331e4-113">Return value</span></span>

<span data-ttu-id="331e4-114">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="331e4-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="331e4-115">Pointeur vers une structure D3DXMATRIX construite à partir du Quaternion source.</span><span class="sxs-lookup"><span data-stu-id="331e4-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="331e4-116">Notes </span><span class="sxs-lookup"><span data-stu-id="331e4-116">Remarks</span></span>

<span data-ttu-id="331e4-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="331e4-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="331e4-118">De cette façon, la fonction D3DXMatrixRotationQuaternion peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="331e4-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="331e4-119">Pour plus d’informations sur le calcul des valeurs de Quaternion à partir d’un vecteur de direction (x, y, z) et d’un angle de rotation, consultez [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="331e4-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="331e4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="331e4-120">Requirements</span></span>



| <span data-ttu-id="331e4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="331e4-121">Requirement</span></span> | <span data-ttu-id="331e4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="331e4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="331e4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="331e4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="331e4-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="331e4-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="331e4-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="331e4-125">Library</span></span><br/> | <dl> <span data-ttu-id="331e4-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="331e4-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="331e4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="331e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331e4-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="331e4-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

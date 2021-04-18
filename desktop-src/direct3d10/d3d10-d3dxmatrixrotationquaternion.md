---
description: Génère une matrice de rotation à partir d’un Quaternion.
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
ms.openlocfilehash: 44cd4a5982b322c2d207263fb490c898ed9fa76e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522981"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="20e36-103">D3DXMatrixRotationQuaternion, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="20e36-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="20e36-104">Génère une matrice de rotation à partir d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="20e36-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20e36-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="20e36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20e36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20e36-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="20e36-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20e36-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20e36-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20e36-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="20e36-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="20e36-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20e36-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e36-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="20e36-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="20e36-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="20e36-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20e36-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20e36-113">Return value</span></span>

<span data-ttu-id="20e36-114">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20e36-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20e36-115">Pointeur vers une structure D3DXMATRIX construite à partir du Quaternion source.</span><span class="sxs-lookup"><span data-stu-id="20e36-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="20e36-116">Notes</span><span class="sxs-lookup"><span data-stu-id="20e36-116">Remarks</span></span>

<span data-ttu-id="20e36-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="20e36-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="20e36-118">De cette façon, la fonction D3DXMatrixRotationQuaternion peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="20e36-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="20e36-119">Pour plus d’informations sur le calcul des valeurs de Quaternion à partir d’un vecteur de direction (x, y, z) et d’un angle de rotation, consultez [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="20e36-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20e36-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20e36-120">Requirements</span></span>



| <span data-ttu-id="20e36-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20e36-121">Requirement</span></span> | <span data-ttu-id="20e36-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="20e36-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20e36-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="20e36-123">Header</span></span><br/>  | <dl> <span data-ttu-id="20e36-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20e36-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="20e36-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20e36-125">Library</span></span><br/> | <dl> <span data-ttu-id="20e36-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20e36-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20e36-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20e36-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e36-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="20e36-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

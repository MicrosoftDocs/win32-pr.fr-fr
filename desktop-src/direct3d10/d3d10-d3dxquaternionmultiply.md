---
description: D3DXQuaternionMultiply, fonction (D3DX10Math. h)-multiplie deux quaternions.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: D3DXQuaternionMultiply, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103157"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="d8308-103">D3DXQuaternionMultiply, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d8308-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="d8308-104">Multiplie deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="d8308-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8308-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8308-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="d8308-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8308-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8308-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8308-108">Type : **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8308-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8308-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d8308-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d8308-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8308-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8308-111">Type : **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8308-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8308-112">Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="d8308-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d8308-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8308-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8308-114">Type : **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8308-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8308-115">Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="d8308-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8308-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8308-116">Return value</span></span>

<span data-ttu-id="d8308-117">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8308-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8308-118">Pointeur vers une structure [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le produit de deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="d8308-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8308-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d8308-119">Remarks</span></span>

<span data-ttu-id="d8308-120">Le résultat représente la rotation Q1 suivie de la rotation Q2 (out = 2e trimestre \* Q1).</span><span class="sxs-lookup"><span data-stu-id="d8308-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="d8308-121">Pour ce faire, **D3DXQuaternionMultiply** conserve la même sémantique que [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) , car les quaternions d’unité peuvent être considérés comme une autre façon de représenter des matrices de rotation.</span><span class="sxs-lookup"><span data-stu-id="d8308-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="d8308-122">Les transformations sont concaténées dans le même ordre pour les fonctions **D3DXQuaternionMultiply** et [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="d8308-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="d8308-123">Par exemple, en supposant que mX et mY représentent les mêmes rotations que qX et qY, m et q représenteront les mêmes rotations.</span><span class="sxs-lookup"><span data-stu-id="d8308-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="d8308-124">La multiplication de quaternions n’est pas commutative.</span><span class="sxs-lookup"><span data-stu-id="d8308-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="d8308-125">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d8308-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d8308-126">De cette façon, la fonction **D3DXQuaternionMultiply** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d8308-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d8308-127">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="d8308-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8308-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8308-128">Requirements</span></span>



| <span data-ttu-id="d8308-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8308-129">Requirement</span></span> | <span data-ttu-id="d8308-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8308-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8308-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8308-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d8308-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8308-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8308-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8308-133">Library</span></span><br/> | <dl> <span data-ttu-id="d8308-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8308-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8308-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8308-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8308-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d8308-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: D3DXQuaternionMultiply, fonction (D3dx9math. h)-multiplie deux quaternions.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: D3DXQuaternionMultiply, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118037"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="da71c-103">D3DXQuaternionMultiply, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="da71c-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="da71c-104">Multiplie deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="da71c-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="da71c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da71c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="da71c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da71c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da71c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da71c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da71c-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="da71c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da71c-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="da71c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da71c-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da71c-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da71c-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="da71c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da71c-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="da71c-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da71c-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da71c-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da71c-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="da71c-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da71c-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="da71c-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da71c-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da71c-116">Return value</span></span>

<span data-ttu-id="da71c-117">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="da71c-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="da71c-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le produit de deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="da71c-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="da71c-119">Notes </span><span class="sxs-lookup"><span data-stu-id="da71c-119">Remarks</span></span>

<span data-ttu-id="da71c-120">Le résultat représente la rotation Q1 suivie de la rotation Q2 (out = 2e trimestre \* Q1).</span><span class="sxs-lookup"><span data-stu-id="da71c-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="da71c-121">Pour ce faire, **D3DXQuaternionMultiply** conserve la même sémantique que [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) , car les quaternions d’unité peuvent être considérés comme une autre façon de représenter des matrices de rotation.</span><span class="sxs-lookup"><span data-stu-id="da71c-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="da71c-122">Les transformations sont concaténées dans le même ordre pour les fonctions **D3DXQuaternionMultiply** et [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="da71c-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="da71c-123">Par exemple, en supposant que mX et mY représentent les mêmes rotations que qX et qY, m et q représenteront les mêmes rotations.</span><span class="sxs-lookup"><span data-stu-id="da71c-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="da71c-124">La multiplication de quaternions n’est pas commutative.</span><span class="sxs-lookup"><span data-stu-id="da71c-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="da71c-125">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="da71c-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="da71c-126">De cette façon, la fonction **D3DXQuaternionMultiply** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="da71c-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="da71c-127">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="da71c-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="da71c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da71c-128">Requirements</span></span>



| <span data-ttu-id="da71c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da71c-129">Requirement</span></span> | <span data-ttu-id="da71c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="da71c-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da71c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="da71c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="da71c-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="da71c-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="da71c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da71c-133">Library</span></span><br/> | <dl> <span data-ttu-id="da71c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da71c-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da71c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da71c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da71c-136">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="da71c-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="da71c-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="da71c-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 





---
description: Génère une matrice de rotation à partir d’un Quaternion.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: D3DXMatrixRotationQuaternion, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525902"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="29074-103">D3DXMatrixRotationQuaternion, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="29074-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="29074-104">Génère une matrice de rotation à partir d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="29074-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="29074-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29074-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="29074-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29074-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="29074-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29074-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="29074-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29074-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="29074-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="29074-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29074-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29074-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29074-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29074-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="29074-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29074-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29074-113">Return value</span></span>

<span data-ttu-id="29074-114">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="29074-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29074-115">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) construite à partir du Quaternion source.</span><span class="sxs-lookup"><span data-stu-id="29074-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="29074-116">Notes</span><span class="sxs-lookup"><span data-stu-id="29074-116">Remarks</span></span>

<span data-ttu-id="29074-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="29074-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="29074-118">De cette façon, la fonction **D3DXMatrixRotationQuaternion** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="29074-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="29074-119">Pour plus d’informations sur le calcul des valeurs de Quaternion à partir d’un vecteur de direction (x, y, z) et d’un angle de rotation, consultez [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="29074-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29074-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29074-120">Requirements</span></span>



| <span data-ttu-id="29074-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29074-121">Requirement</span></span> | <span data-ttu-id="29074-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="29074-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29074-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="29074-123">Header</span></span><br/>  | <dl> <span data-ttu-id="29074-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="29074-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="29074-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29074-125">Library</span></span><br/> | <dl> <span data-ttu-id="29074-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29074-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29074-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29074-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29074-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="29074-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="29074-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="29074-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="29074-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="29074-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="29074-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="29074-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="29074-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="29074-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="29074-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="29074-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 





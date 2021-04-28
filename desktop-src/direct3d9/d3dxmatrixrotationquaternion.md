---
description: 'D3DXMatrixRotationQuaternion, fonction (D3dx9math. h) : génère une matrice de rotation à partir d’un Quaternion.'
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
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118197"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="94498-103">D3DXMatrixRotationQuaternion, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="94498-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="94498-104">Génère une matrice de rotation à partir d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="94498-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="94498-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94498-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="94498-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94498-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="94498-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="94498-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="94498-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="94498-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="94498-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="94498-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94498-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94498-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="94498-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="94498-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="94498-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94498-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="94498-113">Return value</span></span>

<span data-ttu-id="94498-114">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="94498-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="94498-115">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) construite à partir du Quaternion source.</span><span class="sxs-lookup"><span data-stu-id="94498-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="94498-116">Notes </span><span class="sxs-lookup"><span data-stu-id="94498-116">Remarks</span></span>

<span data-ttu-id="94498-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="94498-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="94498-118">De cette façon, la fonction **D3DXMatrixRotationQuaternion** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="94498-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="94498-119">Pour plus d’informations sur le calcul des valeurs de Quaternion à partir d’un vecteur de direction (x, y, z) et d’un angle de rotation, consultez [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="94498-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94498-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94498-120">Requirements</span></span>



| <span data-ttu-id="94498-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94498-121">Requirement</span></span> | <span data-ttu-id="94498-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="94498-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94498-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="94498-123">Header</span></span><br/>  | <dl> <span data-ttu-id="94498-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="94498-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="94498-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94498-125">Library</span></span><br/> | <dl> <span data-ttu-id="94498-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94498-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94498-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94498-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94498-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="94498-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="94498-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="94498-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="94498-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="94498-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="94498-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="94498-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="94498-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="94498-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="94498-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="94498-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 





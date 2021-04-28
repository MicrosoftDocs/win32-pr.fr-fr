---
description: 'D3DXMatrixLookAtLH, fonction (D3dx9math. h) : génère une matrice de gauche et de droite.'
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: D3DXMatrixLookAtLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a423e700c4a42e2ae7f7e522d83a5a4bd9bf3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107587"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="541c1-103">D3DXMatrixLookAtLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="541c1-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="541c1-104">Crée une matrice de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="541c1-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="541c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="541c1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="541c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="541c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541c1-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="541c1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="541c1-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="541c1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="541c1-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="541c1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="541c1-110">*pEye* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="541c1-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c1-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="541c1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="541c1-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le point oculaire.</span><span class="sxs-lookup"><span data-stu-id="541c1-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="541c1-113">Cette valeur est utilisée dans la traduction.</span><span class="sxs-lookup"><span data-stu-id="541c1-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="541c1-114">*pAt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="541c1-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c1-115">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="541c1-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="541c1-116">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit la cible de l’apparence de la caméra.</span><span class="sxs-lookup"><span data-stu-id="541c1-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="541c1-117">*pUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="541c1-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c1-118">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="541c1-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="541c1-119">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le monde actuel, généralement \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="541c1-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541c1-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="541c1-120">Return value</span></span>

<span data-ttu-id="541c1-121">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="541c1-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="541c1-122">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de recherche gauche.</span><span class="sxs-lookup"><span data-stu-id="541c1-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="541c1-123">Notes </span><span class="sxs-lookup"><span data-stu-id="541c1-123">Remarks</span></span>

<span data-ttu-id="541c1-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="541c1-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="541c1-125">De cette façon, la fonction **D3DXMatrixLookAtLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="541c1-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="541c1-126">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="541c1-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="541c1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="541c1-127">Requirements</span></span>



| <span data-ttu-id="541c1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="541c1-128">Requirement</span></span> | <span data-ttu-id="541c1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="541c1-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="541c1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="541c1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="541c1-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="541c1-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="541c1-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="541c1-132">Library</span></span><br/> | <dl> <span data-ttu-id="541c1-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="541c1-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="541c1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="541c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541c1-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="541c1-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="541c1-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="541c1-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 





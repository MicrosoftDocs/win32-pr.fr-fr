---
description: Crée une matrice de gauche et de droite.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: D3DXMatrixLookAtLH, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a5a7ffa8750fb08174f45b1069f103bfe08be1f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531041"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="971bc-103">D3DXMatrixLookAtLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="971bc-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="971bc-104">Crée une matrice de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="971bc-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="971bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="971bc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="971bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="971bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="971bc-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="971bc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="971bc-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="971bc-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="971bc-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="971bc-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="971bc-110">*pEye* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="971bc-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971bc-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="971bc-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="971bc-112">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui définit le point oculaire.</span><span class="sxs-lookup"><span data-stu-id="971bc-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="971bc-113">Cette valeur est utilisée dans la traduction.</span><span class="sxs-lookup"><span data-stu-id="971bc-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="971bc-114">*pAt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="971bc-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971bc-115">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="971bc-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="971bc-116">Pointeur vers la structure D3DXVECTOR3 qui définit la cible de l’apparence de la caméra.</span><span class="sxs-lookup"><span data-stu-id="971bc-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="971bc-117">*pUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="971bc-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971bc-118">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="971bc-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="971bc-119">Pointeur vers la structure D3DXVECTOR3 qui définit le monde actuel, généralement \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="971bc-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="971bc-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="971bc-120">Return value</span></span>

<span data-ttu-id="971bc-121">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="971bc-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="971bc-122">Pointeur vers une structure D3DXMATRIX qui est une matrice de recherche gauche.</span><span class="sxs-lookup"><span data-stu-id="971bc-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="971bc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="971bc-123">Remarks</span></span>

<span data-ttu-id="971bc-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="971bc-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="971bc-125">De cette façon, la fonction D3DXMatrixLookAtLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="971bc-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="971bc-126">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="971bc-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="971bc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="971bc-127">Requirements</span></span>



| <span data-ttu-id="971bc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="971bc-128">Requirement</span></span> | <span data-ttu-id="971bc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="971bc-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="971bc-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="971bc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="971bc-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="971bc-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="971bc-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="971bc-132">Library</span></span><br/> | <dl> <span data-ttu-id="971bc-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="971bc-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="971bc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="971bc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971bc-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="971bc-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

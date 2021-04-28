---
description: 'D3DXMatrixLookAtRH, fonction (D3DX10Math. h) : génère une matrice de droite et de gauche.'
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: D3DXMatrixLookAtRH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0380207124e4a446b6303dbb377d116b8ae058ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103447"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="0a951-103">D3DXMatrixLookAtRH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0a951-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="0a951-104">Génère une matrice de droite et de gauche.</span><span class="sxs-lookup"><span data-stu-id="0a951-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a951-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a951-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="0a951-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a951-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0a951-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a951-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a951-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0a951-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0a951-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0a951-110">*pEye* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a951-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a951-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a951-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a951-112">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui définit le point oculaire.</span><span class="sxs-lookup"><span data-stu-id="0a951-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="0a951-113">Cette valeur est utilisée dans la traduction.</span><span class="sxs-lookup"><span data-stu-id="0a951-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="0a951-114">*pAt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a951-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a951-115">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a951-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a951-116">Pointeur vers la structure D3DXVECTOR3 qui définit la cible de l’apparence de la caméra.</span><span class="sxs-lookup"><span data-stu-id="0a951-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="0a951-117">*pUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a951-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a951-118">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a951-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a951-119">Pointeur vers la structure D3DXVECTOR3 qui définit le monde actuel, généralement \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="0a951-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a951-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0a951-120">Return value</span></span>

<span data-ttu-id="0a951-121">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a951-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0a951-122">Pointeur vers une structure D3DXMATRIX qui est une matrice de recherche à droite.</span><span class="sxs-lookup"><span data-stu-id="0a951-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a951-123">Notes </span><span class="sxs-lookup"><span data-stu-id="0a951-123">Remarks</span></span>

<span data-ttu-id="0a951-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="0a951-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0a951-125">De cette façon, la fonction D3DXMatrixLookAtRH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0a951-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0a951-126">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="0a951-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="0a951-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a951-127">Requirements</span></span>



| <span data-ttu-id="0a951-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a951-128">Requirement</span></span> | <span data-ttu-id="0a951-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a951-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a951-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a951-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0a951-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a951-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0a951-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a951-132">Library</span></span><br/> | <dl> <span data-ttu-id="0a951-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a951-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a951-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a951-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a951-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0a951-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

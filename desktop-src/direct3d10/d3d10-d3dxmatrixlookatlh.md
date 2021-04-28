---
description: 'D3DXMatrixLookAtLH, fonction (D3DX10Math. h) : génère une matrice de gauche et de droite.'
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
ms.openlocfilehash: 3590d2cbdeead9e1b9b2547b2344163b81f05d11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109167"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="db65c-103">D3DXMatrixLookAtLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="db65c-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="db65c-104">Crée une matrice de gauche et de droite.</span><span class="sxs-lookup"><span data-stu-id="db65c-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="db65c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db65c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="db65c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db65c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db65c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="db65c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db65c-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="db65c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db65c-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="db65c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="db65c-110">*pEye* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db65c-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db65c-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="db65c-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="db65c-112">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui définit le point oculaire.</span><span class="sxs-lookup"><span data-stu-id="db65c-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="db65c-113">Cette valeur est utilisée dans la traduction.</span><span class="sxs-lookup"><span data-stu-id="db65c-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="db65c-114">*pAt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db65c-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db65c-115">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="db65c-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="db65c-116">Pointeur vers la structure D3DXVECTOR3 qui définit la cible de l’apparence de la caméra.</span><span class="sxs-lookup"><span data-stu-id="db65c-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="db65c-117">*pUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db65c-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db65c-118">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="db65c-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="db65c-119">Pointeur vers la structure D3DXVECTOR3 qui définit le monde actuel, généralement \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="db65c-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db65c-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db65c-120">Return value</span></span>

<span data-ttu-id="db65c-121">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="db65c-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db65c-122">Pointeur vers une structure D3DXMATRIX qui est une matrice de recherche gauche.</span><span class="sxs-lookup"><span data-stu-id="db65c-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="db65c-123">Notes </span><span class="sxs-lookup"><span data-stu-id="db65c-123">Remarks</span></span>

<span data-ttu-id="db65c-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="db65c-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="db65c-125">De cette façon, la fonction D3DXMatrixLookAtLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="db65c-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="db65c-126">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="db65c-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="db65c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db65c-127">Requirements</span></span>



| <span data-ttu-id="db65c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db65c-128">Requirement</span></span> | <span data-ttu-id="db65c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="db65c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db65c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="db65c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="db65c-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="db65c-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="db65c-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db65c-132">Library</span></span><br/> | <dl> <span data-ttu-id="db65c-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db65c-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db65c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db65c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db65c-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="db65c-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

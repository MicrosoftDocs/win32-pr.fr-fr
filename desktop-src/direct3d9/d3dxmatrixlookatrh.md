---
description: Génère une matrice de droite et de gauche.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: D3DXMatrixLookAtRH, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f09b57d46c6c5dea51c9b55ce6fe507d5bfe415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322658"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="0bc03-103">D3DXMatrixLookAtRH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0bc03-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="0bc03-104">Génère une matrice de droite et de gauche.</span><span class="sxs-lookup"><span data-stu-id="0bc03-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc03-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bc03-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="0bc03-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bc03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc03-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0bc03-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc03-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bc03-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bc03-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0bc03-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0bc03-110">*pEye* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bc03-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc03-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bc03-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bc03-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le point oculaire.</span><span class="sxs-lookup"><span data-stu-id="0bc03-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="0bc03-113">Cette valeur est utilisée dans la traduction.</span><span class="sxs-lookup"><span data-stu-id="0bc03-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="0bc03-114">*pAt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bc03-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc03-115">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bc03-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bc03-116">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit la cible de l’apparence de la caméra.</span><span class="sxs-lookup"><span data-stu-id="0bc03-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="0bc03-117">*pUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bc03-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc03-118">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bc03-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bc03-119">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui définit le monde actuel, généralement \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="0bc03-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc03-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bc03-120">Return value</span></span>

<span data-ttu-id="0bc03-121">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bc03-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bc03-122">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de recherche à droite.</span><span class="sxs-lookup"><span data-stu-id="0bc03-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc03-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0bc03-123">Remarks</span></span>

<span data-ttu-id="0bc03-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="0bc03-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0bc03-125">De cette façon, la fonction **D3DXMatrixLookAtRH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0bc03-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0bc03-126">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="0bc03-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="0bc03-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bc03-127">Requirements</span></span>



| <span data-ttu-id="0bc03-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bc03-128">Requirement</span></span> | <span data-ttu-id="0bc03-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc03-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc03-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bc03-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc03-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc03-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc03-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bc03-132">Library</span></span><br/> | <dl> <span data-ttu-id="0bc03-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc03-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bc03-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bc03-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc03-135">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0bc03-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0bc03-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="0bc03-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 





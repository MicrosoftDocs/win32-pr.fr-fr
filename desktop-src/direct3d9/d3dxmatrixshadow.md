---
description: Crée une matrice qui aplatit la géométrie dans un plan.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: D3DXMatrixShadow, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539876"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="ebdfb-103">D3DXMatrixShadow, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ebdfb-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="ebdfb-104">Crée une matrice qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebdfb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebdfb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="ebdfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebdfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebdfb-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ebdfb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebdfb-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebdfb-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebdfb-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ebdfb-110">*pLight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebdfb-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebdfb-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebdfb-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ebdfb-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) décrivant la position de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="ebdfb-113">*pPlane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebdfb-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebdfb-114">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebdfb-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="ebdfb-115">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebdfb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebdfb-116">Return value</span></span>

<span data-ttu-id="ebdfb-117">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebdfb-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebdfb-118">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebdfb-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ebdfb-119">Remarks</span></span>

<span data-ttu-id="ebdfb-120">La fonction **D3DXMatrixShadow** aplatit la géométrie dans un plan, comme s’il s’agissait d’une ombre à partir d’une lumière.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="ebdfb-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="ebdfb-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ebdfb-122">De cette façon, la fonction **D3DXMatrixShadow** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ebdfb-123">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="ebdfb-124">Si le composant w de la lumière est égal à 0, le rayon de l’origine à la lumière représente une lumière directionnelle.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="ebdfb-125">S’il s’agit de 1, la lumière est une lumière de point.</span><span class="sxs-lookup"><span data-stu-id="ebdfb-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdfb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebdfb-126">Requirements</span></span>



| <span data-ttu-id="ebdfb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebdfb-127">Requirement</span></span> | <span data-ttu-id="ebdfb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebdfb-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdfb-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebdfb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ebdfb-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebdfb-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ebdfb-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebdfb-131">Library</span></span><br/> | <dl> <span data-ttu-id="ebdfb-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebdfb-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ebdfb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebdfb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdfb-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ebdfb-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 





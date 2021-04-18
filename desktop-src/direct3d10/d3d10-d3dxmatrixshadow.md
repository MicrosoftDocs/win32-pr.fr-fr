---
description: Crée une matrice qui aplatit la géométrie dans un plan.
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: D3DXMatrixShadow, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2edaee98f5a56cf5dffec262ecc3d546f0116f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323242"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a><span data-ttu-id="cce14-103">D3DXMatrixShadow, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cce14-103">D3DXMatrixShadow function (D3DX10Math.h)</span></span>

<span data-ttu-id="cce14-104">Crée une matrice qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="cce14-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce14-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cce14-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="cce14-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cce14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce14-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cce14-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cce14-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cce14-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cce14-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cce14-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cce14-110">*pLight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cce14-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce14-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cce14-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="cce14-112">Pointeur vers un [**D3DXVECTOR4**](d3d10-d3dxvector4.md) décrivant la position de la lumière.</span><span class="sxs-lookup"><span data-stu-id="cce14-112">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="cce14-113">*pPlane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cce14-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce14-114">Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="cce14-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cce14-115">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md)source.</span><span class="sxs-lookup"><span data-stu-id="cce14-115">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce14-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cce14-116">Return value</span></span>

<span data-ttu-id="cce14-117">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cce14-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cce14-118">Pointeur vers une structure D3DXMATRIX qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="cce14-118">Pointer to a D3DXMATRIX structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce14-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cce14-119">Remarks</span></span>

<span data-ttu-id="cce14-120">La fonction **D3DXMatrixShadow** aplatit la géométrie dans un plan, comme s’il s’agissait d’une ombre à partir d’une lumière.</span><span class="sxs-lookup"><span data-stu-id="cce14-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="cce14-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="cce14-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cce14-122">De cette façon, la fonction **D3DXMatrixShadow** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="cce14-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cce14-123">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="cce14-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="cce14-124">Si le composant w de la lumière est égal à 0, le rayon de l’origine à la lumière représente une lumière directionnelle.</span><span class="sxs-lookup"><span data-stu-id="cce14-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="cce14-125">S’il s’agit de 1, la lumière est une lumière de point.</span><span class="sxs-lookup"><span data-stu-id="cce14-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce14-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cce14-126">Requirements</span></span>



| <span data-ttu-id="cce14-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cce14-127">Requirement</span></span> | <span data-ttu-id="cce14-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cce14-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cce14-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="cce14-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cce14-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce14-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cce14-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cce14-131">Library</span></span><br/> | <dl> <span data-ttu-id="cce14-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cce14-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cce14-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cce14-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce14-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cce14-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: 'D3DXMatrixShadow, fonction (D3dx9math. h) : crée une matrice qui aplatit la géométrie dans un plan.'
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
ms.openlocfilehash: 111a1448f62cae3f782917de76d92e88aa5a3356
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118057"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="396f1-103">D3DXMatrixShadow, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="396f1-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="396f1-104">Crée une matrice qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="396f1-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="396f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="396f1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="396f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="396f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396f1-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="396f1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="396f1-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="396f1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="396f1-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="396f1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="396f1-110">*pLight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="396f1-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396f1-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="396f1-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="396f1-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) décrivant la position de la lumière.</span><span class="sxs-lookup"><span data-stu-id="396f1-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="396f1-113">*pPlane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="396f1-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396f1-114">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="396f1-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="396f1-115">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) source.</span><span class="sxs-lookup"><span data-stu-id="396f1-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396f1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="396f1-116">Return value</span></span>

<span data-ttu-id="396f1-117">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="396f1-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="396f1-118">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui aplatit la géométrie dans un plan.</span><span class="sxs-lookup"><span data-stu-id="396f1-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="396f1-119">Notes </span><span class="sxs-lookup"><span data-stu-id="396f1-119">Remarks</span></span>

<span data-ttu-id="396f1-120">La fonction **D3DXMatrixShadow** aplatit la géométrie dans un plan, comme s’il s’agissait d’une ombre à partir d’une lumière.</span><span class="sxs-lookup"><span data-stu-id="396f1-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="396f1-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="396f1-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="396f1-122">De cette façon, la fonction **D3DXMatrixShadow** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="396f1-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="396f1-123">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="396f1-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="396f1-124">Si le composant w de la lumière est égal à 0, le rayon de l’origine à la lumière représente une lumière directionnelle.</span><span class="sxs-lookup"><span data-stu-id="396f1-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="396f1-125">S’il s’agit de 1, la lumière est une lumière de point.</span><span class="sxs-lookup"><span data-stu-id="396f1-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="396f1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="396f1-126">Requirements</span></span>



| <span data-ttu-id="396f1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="396f1-127">Requirement</span></span> | <span data-ttu-id="396f1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="396f1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="396f1-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="396f1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="396f1-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="396f1-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="396f1-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="396f1-131">Library</span></span><br/> | <dl> <span data-ttu-id="396f1-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="396f1-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="396f1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="396f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396f1-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="396f1-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 





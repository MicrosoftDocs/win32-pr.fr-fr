---
description: 'D3DXPlaneFromPointNormal, fonction (D3dx9math. h) : construit un plan à partir d’un point et d’un normal.'
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098087"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="188aa-103">D3DXPlaneFromPointNormal, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="188aa-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="188aa-104">Construit un plan à partir d’un point et d’un normal.</span><span class="sxs-lookup"><span data-stu-id="188aa-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="188aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="188aa-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="188aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="188aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="188aa-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="188aa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="188aa-108">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="188aa-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="188aa-109">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="188aa-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="188aa-110">*PPoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="188aa-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="188aa-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="188aa-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="188aa-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le point utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="188aa-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="188aa-113">*pNormal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="188aa-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="188aa-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="188aa-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="188aa-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , définissant le normal utilisé pour construire le plan.</span><span class="sxs-lookup"><span data-stu-id="188aa-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="188aa-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="188aa-116">Return value</span></span>

<span data-ttu-id="188aa-117">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="188aa-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="188aa-118">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) construite à partir du point et du normal.</span><span class="sxs-lookup"><span data-stu-id="188aa-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="188aa-119">Notes </span><span class="sxs-lookup"><span data-stu-id="188aa-119">Remarks</span></span>

<span data-ttu-id="188aa-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="188aa-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="188aa-121">De cette façon, la fonction **D3DXPlaneFromPointNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="188aa-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="188aa-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="188aa-122">Requirements</span></span>



| <span data-ttu-id="188aa-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="188aa-123">Requirement</span></span> | <span data-ttu-id="188aa-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="188aa-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="188aa-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="188aa-125">Header</span></span><br/>  | <dl> <span data-ttu-id="188aa-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="188aa-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="188aa-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="188aa-127">Library</span></span><br/> | <dl> <span data-ttu-id="188aa-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="188aa-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="188aa-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="188aa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188aa-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="188aa-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="188aa-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="188aa-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 





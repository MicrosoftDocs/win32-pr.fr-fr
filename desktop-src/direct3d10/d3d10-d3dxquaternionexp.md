---
description: 'Fonction D3DXQuaternionExp (D3DX10Math. h) : calcule la valeur exponentielle.'
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: D3DXQuaternionExp, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7c022b9df4302683a184b4fc8329561b22d341d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103217"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="19c37-103">D3DXQuaternionExp, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="19c37-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="19c37-104">Calcule la valeur exponentielle.</span><span class="sxs-lookup"><span data-stu-id="19c37-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19c37-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="19c37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c37-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="19c37-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19c37-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="19c37-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19c37-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="19c37-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19c37-110">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19c37-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c37-111">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="19c37-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19c37-112">Pointeur vers la structure D3DXQUATERNION source.</span><span class="sxs-lookup"><span data-stu-id="19c37-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c37-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="19c37-113">Return value</span></span>

<span data-ttu-id="19c37-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="19c37-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="19c37-115">Pointeur vers une structure D3DXQUATERNION qui est l’exponentiel.</span><span class="sxs-lookup"><span data-stu-id="19c37-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c37-116">Notes </span><span class="sxs-lookup"><span data-stu-id="19c37-116">Remarks</span></span>

<span data-ttu-id="19c37-117">Cette méthode convertit un Quaternion pur en un Quaternion d’unité.</span><span class="sxs-lookup"><span data-stu-id="19c37-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="19c37-118">D3DXQuaternionExp attend un Quaternion pur, où w est ignoré dans le calcul (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="19c37-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="19c37-119">où v est la partie vectorielle d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="19c37-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="19c37-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="19c37-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="19c37-121">De cette façon, la fonction D3DXQuaternionExp peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="19c37-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="19c37-122">La méthode [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) peut également être utilisée pour configurer les points de contrôle d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="19c37-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="19c37-123">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="19c37-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c37-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19c37-124">Requirements</span></span>



| <span data-ttu-id="19c37-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19c37-125">Requirement</span></span> | <span data-ttu-id="19c37-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="19c37-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c37-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="19c37-127">Header</span></span><br/>  | <dl> <span data-ttu-id="19c37-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c37-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="19c37-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19c37-129">Library</span></span><br/> | <dl> <span data-ttu-id="19c37-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19c37-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19c37-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19c37-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c37-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="19c37-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: Génère un Quaternion à partir d’une matrice de rotation.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: D3DXQuaternionRotationMatrix, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211900"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="9940f-103">D3DXQuaternionRotationMatrix, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9940f-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="9940f-104">Génère un Quaternion à partir d’une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="9940f-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9940f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9940f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="9940f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9940f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9940f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9940f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9940f-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9940f-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9940f-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9940f-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9940f-110">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9940f-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9940f-111">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9940f-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9940f-112">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="9940f-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9940f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9940f-113">Return value</span></span>

<span data-ttu-id="9940f-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9940f-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9940f-115">Pointeur vers la structure D3DXQUATERNION construite à partir d’une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="9940f-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9940f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9940f-116">Remarks</span></span>

<span data-ttu-id="9940f-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="9940f-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9940f-118">De cette façon, la fonction D3DXQuaternionRotationMatrix peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="9940f-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9940f-119">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="9940f-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9940f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9940f-120">Requirements</span></span>



| <span data-ttu-id="9940f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9940f-121">Requirement</span></span> | <span data-ttu-id="9940f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9940f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9940f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9940f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9940f-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9940f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9940f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9940f-125">Library</span></span><br/> | <dl> <span data-ttu-id="9940f-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9940f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9940f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9940f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9940f-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="9940f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

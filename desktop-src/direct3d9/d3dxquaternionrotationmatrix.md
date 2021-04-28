---
description: 'D3DXQuaternionRotationMatrix, fonction (D3dx9math. h) : génère un Quaternion à partir d’une matrice de rotation.'
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: D3DXQuaternionRotationMatrix, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0ff8529f32d398ac208cff3214fccfdb2ade81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094007"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="e2755-103">D3DXQuaternionRotationMatrix, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e2755-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="e2755-104">Génère un Quaternion à partir d’une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="e2755-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2755-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2755-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e2755-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2755-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2755-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2755-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2755-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2755-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2755-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e2755-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2755-110">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2755-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2755-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2755-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e2755-112">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="e2755-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2755-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2755-113">Return value</span></span>

<span data-ttu-id="e2755-114">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2755-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2755-115">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) construite à partir d’une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="e2755-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2755-116">Notes </span><span class="sxs-lookup"><span data-stu-id="e2755-116">Remarks</span></span>

<span data-ttu-id="e2755-117">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="e2755-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e2755-118">De cette façon, la fonction **D3DXQuaternionRotationMatrix** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e2755-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e2755-119">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="e2755-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2755-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2755-120">Requirements</span></span>



| <span data-ttu-id="e2755-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2755-121">Requirement</span></span> | <span data-ttu-id="e2755-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2755-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2755-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2755-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e2755-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2755-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e2755-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2755-125">Library</span></span><br/> | <dl> <span data-ttu-id="e2755-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2755-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2755-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2755-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2755-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e2755-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e2755-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="e2755-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="e2755-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e2755-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 





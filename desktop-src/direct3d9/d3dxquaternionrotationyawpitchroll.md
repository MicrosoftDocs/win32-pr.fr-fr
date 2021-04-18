---
description: Génère un Quaternion avec le lacet, le tangage et le roulis donnés.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522588"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="9e57e-103">D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9e57e-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="9e57e-104">Génère un Quaternion avec le lacet, le tangage et le roulis donnés.</span><span class="sxs-lookup"><span data-stu-id="9e57e-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e57e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e57e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="9e57e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e57e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e57e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9e57e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57e-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e57e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9e57e-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9e57e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9e57e-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e57e-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e57e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e57e-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="9e57e-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="9e57e-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e57e-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e57e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e57e-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="9e57e-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="9e57e-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e57e-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57e-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e57e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e57e-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="9e57e-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e57e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e57e-119">Return value</span></span>

<span data-ttu-id="9e57e-120">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e57e-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9e57e-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9e57e-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e57e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="9e57e-122">Remarks</span></span>

<span data-ttu-id="9e57e-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="9e57e-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9e57e-124">De cette façon, la fonction **D3DXQuaternionRotationYawPitchRoll** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="9e57e-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9e57e-125">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="9e57e-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e57e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e57e-126">Requirements</span></span>



| <span data-ttu-id="9e57e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e57e-127">Requirement</span></span> | <span data-ttu-id="9e57e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e57e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e57e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e57e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9e57e-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e57e-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9e57e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e57e-131">Library</span></span><br/> | <dl> <span data-ttu-id="9e57e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e57e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e57e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e57e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e57e-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="9e57e-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9e57e-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="9e57e-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="9e57e-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="9e57e-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 

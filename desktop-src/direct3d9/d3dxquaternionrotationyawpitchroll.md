---
description: 'D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h) : génère un Quaternion avec le lacet, le tangage et le roulis donnés.'
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
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117997"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="26065-103">D3DXQuaternionRotationYawPitchRoll, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="26065-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="26065-104">Génère un Quaternion avec le lacet, le tangage et le roulis donnés.</span><span class="sxs-lookup"><span data-stu-id="26065-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="26065-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26065-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="26065-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26065-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26065-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26065-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="26065-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="26065-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="26065-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="26065-110">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26065-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26065-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26065-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26065-112">Lacet autour de l’axe y, en radians.</span><span class="sxs-lookup"><span data-stu-id="26065-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="26065-113">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26065-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26065-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26065-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26065-115">Hauteur autour de l’axe x, en radians.</span><span class="sxs-lookup"><span data-stu-id="26065-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="26065-116">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26065-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26065-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26065-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26065-118">Tourner autour de l’axe z, en radians.</span><span class="sxs-lookup"><span data-stu-id="26065-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26065-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="26065-119">Return value</span></span>

<span data-ttu-id="26065-120">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="26065-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="26065-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) avec le lacet, le tangage et le roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="26065-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="26065-122">Notes </span><span class="sxs-lookup"><span data-stu-id="26065-122">Remarks</span></span>

<span data-ttu-id="26065-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="26065-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="26065-124">De cette façon, la fonction **D3DXQuaternionRotationYawPitchRoll** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="26065-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="26065-125">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="26065-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="26065-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26065-126">Requirements</span></span>



| <span data-ttu-id="26065-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26065-127">Requirement</span></span> | <span data-ttu-id="26065-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="26065-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26065-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="26065-129">Header</span></span><br/>  | <dl> <span data-ttu-id="26065-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26065-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="26065-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26065-131">Library</span></span><br/> | <dl> <span data-ttu-id="26065-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26065-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26065-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26065-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26065-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="26065-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="26065-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="26065-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="26065-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="26065-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 

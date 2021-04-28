---
description: 'Fonction D3DXQuaternionToAxisAngle (D3DX10Math. h) : calcule l’axe et l’angle de rotation d’un Quaternion.'
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: D3DXQuaternionToAxisAngle, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108697"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="2530a-103">D3DXQuaternionToAxisAngle, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2530a-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="2530a-104">Calcule l’axe et l’angle de rotation d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="2530a-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2530a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2530a-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="2530a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2530a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2530a-107">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2530a-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2530a-108">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2530a-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2530a-109">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)source.</span><span class="sxs-lookup"><span data-stu-id="2530a-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="2530a-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2530a-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2530a-111">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2530a-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2530a-112">Cette fonction retourne un pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui identifie l’axe de rotation du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="2530a-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="2530a-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2530a-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2530a-114">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2530a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2530a-115">Cette fonction retourne un pointeur vers une valeur FLOAT qui identifie l’angle de rotation du quaternion en radians.</span><span class="sxs-lookup"><span data-stu-id="2530a-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2530a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2530a-116">Return value</span></span>

<span data-ttu-id="2530a-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2530a-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2530a-118">Notes </span><span class="sxs-lookup"><span data-stu-id="2530a-118">Remarks</span></span>

<span data-ttu-id="2530a-119">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="2530a-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2530a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2530a-120">Requirements</span></span>



| <span data-ttu-id="2530a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2530a-121">Requirement</span></span> | <span data-ttu-id="2530a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2530a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2530a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2530a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2530a-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2530a-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2530a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2530a-125">Library</span></span><br/> | <dl> <span data-ttu-id="2530a-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2530a-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2530a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2530a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2530a-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2530a-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

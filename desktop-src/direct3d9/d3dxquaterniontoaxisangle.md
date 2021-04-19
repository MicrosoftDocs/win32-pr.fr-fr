---
description: Calcule l’axe et l’angle de rotation d’un Quaternion.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: D3DXQuaternionToAxisAngle, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538505"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="fca87-103">D3DXQuaternionToAxisAngle, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fca87-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="fca87-104">Calcule l’axe et l’angle de rotation d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fca87-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca87-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="fca87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fca87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca87-107">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fca87-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca87-108">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fca87-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fca87-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="fca87-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fca87-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fca87-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fca87-111">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fca87-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fca87-112">Cette fonction retourne un pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui identifie l’axe de rotation du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fca87-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="fca87-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fca87-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fca87-114">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fca87-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fca87-115">Cette fonction retourne un pointeur vers une valeur FLOAT qui identifie l’angle de rotation du quaternion en radians.</span><span class="sxs-lookup"><span data-stu-id="fca87-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca87-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fca87-116">Return value</span></span>

<span data-ttu-id="fca87-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fca87-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fca87-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fca87-118">Remarks</span></span>

<span data-ttu-id="fca87-119">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="fca87-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca87-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fca87-120">Requirements</span></span>



| <span data-ttu-id="fca87-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fca87-121">Requirement</span></span> | <span data-ttu-id="fca87-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fca87-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fca87-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fca87-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fca87-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca87-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fca87-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fca87-125">Library</span></span><br/> | <dl> <span data-ttu-id="fca87-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fca87-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fca87-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fca87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca87-128">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fca87-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

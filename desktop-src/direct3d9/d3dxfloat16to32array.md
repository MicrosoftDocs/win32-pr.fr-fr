---
description: Convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: D3DXFloat16To32Array, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542161"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="08401-103">D3DXFloat16To32Array, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="08401-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="08401-104">Convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="08401-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="08401-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08401-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="08401-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08401-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08401-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08401-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="08401-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="08401-109">Pointeur vers le tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="08401-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="08401-110">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08401-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08401-111">Type : **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="08401-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="08401-112">Pointeur vers un tableau de valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="08401-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="08401-113">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08401-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08401-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08401-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08401-115">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="08401-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08401-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08401-116">Return value</span></span>

<span data-ttu-id="08401-117">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="08401-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="08401-118">Pointeur vers un tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="08401-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="08401-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08401-119">Requirements</span></span>



| <span data-ttu-id="08401-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08401-120">Requirement</span></span> | <span data-ttu-id="08401-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="08401-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08401-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="08401-122">Header</span></span><br/>  | <dl> <span data-ttu-id="08401-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="08401-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="08401-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08401-124">Library</span></span><br/> | <dl> <span data-ttu-id="08401-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08401-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="08401-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08401-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08401-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="08401-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

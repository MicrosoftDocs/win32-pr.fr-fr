---
description: Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: D3DXFloat32To16Array, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523825"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="12fee-103">D3DXFloat32To16Array, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="12fee-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="12fee-104">Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="12fee-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12fee-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="12fee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12fee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fee-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="12fee-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12fee-108">Type : **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="12fee-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="12fee-109">Pointeur vers le tableau de valeurs float de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="12fee-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="12fee-110">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12fee-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fee-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12fee-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12fee-112">Pointeur vers un tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="12fee-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="12fee-113">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12fee-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fee-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12fee-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12fee-115">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="12fee-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fee-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12fee-116">Return value</span></span>

<span data-ttu-id="12fee-117">Type : **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="12fee-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="12fee-118">Pointeur vers un tableau de valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="12fee-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fee-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12fee-119">Requirements</span></span>



| <span data-ttu-id="12fee-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12fee-120">Requirement</span></span> | <span data-ttu-id="12fee-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="12fee-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12fee-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="12fee-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12fee-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fee-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="12fee-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12fee-124">Library</span></span><br/> | <dl> <span data-ttu-id="12fee-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12fee-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12fee-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12fee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fee-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="12fee-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

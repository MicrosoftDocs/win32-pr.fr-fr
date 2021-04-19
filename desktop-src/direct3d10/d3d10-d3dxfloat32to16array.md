---
description: Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: D3DXFloat32To16Array, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545892"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="f177c-103">D3DXFloat32To16Array, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f177c-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="f177c-104">Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f177c-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="f177c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f177c-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="f177c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f177c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f177c-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f177c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f177c-108">Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="f177c-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="f177c-109">Pointeur vers le tableau de valeurs float de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f177c-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="f177c-110">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f177c-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f177c-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f177c-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f177c-112">Pointeur vers un tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f177c-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="f177c-113">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f177c-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f177c-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f177c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f177c-115">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f177c-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f177c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f177c-116">Return value</span></span>

<span data-ttu-id="f177c-117">Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="f177c-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="f177c-118">Pointeur vers un tableau de valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f177c-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f177c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f177c-119">Requirements</span></span>



| <span data-ttu-id="f177c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f177c-120">Requirement</span></span> | <span data-ttu-id="f177c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f177c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f177c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f177c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f177c-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f177c-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f177c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f177c-124">Library</span></span><br/> | <dl> <span data-ttu-id="f177c-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f177c-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f177c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f177c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f177c-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f177c-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: 'D3DXFloat16To32Array, fonction (D3dx9math. h) : convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.'
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
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107597"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="0522b-103">D3DXFloat16To32Array, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0522b-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="0522b-104">Convertit un tableau de valeurs float de 16 bits en valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0522b-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0522b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0522b-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0522b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0522b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0522b-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0522b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0522b-108">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0522b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0522b-109">Pointeur vers le tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0522b-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0522b-110">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0522b-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0522b-111">Type : **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="0522b-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0522b-112">Pointeur vers un tableau de valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0522b-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0522b-113">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0522b-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0522b-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0522b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0522b-115">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="0522b-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0522b-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0522b-116">Return value</span></span>

<span data-ttu-id="0522b-117">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0522b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0522b-118">Pointeur vers un tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0522b-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0522b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0522b-119">Requirements</span></span>



| <span data-ttu-id="0522b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0522b-120">Requirement</span></span> | <span data-ttu-id="0522b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0522b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0522b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0522b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0522b-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0522b-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0522b-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0522b-124">Library</span></span><br/> | <dl> <span data-ttu-id="0522b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0522b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0522b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0522b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0522b-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0522b-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

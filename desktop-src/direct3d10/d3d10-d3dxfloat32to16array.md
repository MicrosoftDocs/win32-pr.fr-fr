---
description: 'D3DXFloat32To16Array, fonction (D3DX10Math. h) : convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.'
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
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103517"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="b5f07-103">D3DXFloat32To16Array, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b5f07-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="b5f07-104">Convertit un tableau de valeurs float 32 bits en valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f07-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5f07-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="b5f07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5f07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f07-107">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5f07-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f07-108">Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5f07-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="b5f07-109">Pointeur vers le tableau de valeurs float de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f07-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="b5f07-110">*code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5f07-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f07-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5f07-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b5f07-112">Pointeur vers un tableau de valeurs float 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f07-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="b5f07-113">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5f07-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f07-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5f07-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5f07-115">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b5f07-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f07-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5f07-116">Return value</span></span>

<span data-ttu-id="b5f07-117">Type : **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5f07-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="b5f07-118">Pointeur vers un tableau de valeurs float 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f07-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f07-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5f07-119">Requirements</span></span>



| <span data-ttu-id="b5f07-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5f07-120">Requirement</span></span> | <span data-ttu-id="b5f07-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f07-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f07-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5f07-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b5f07-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f07-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5f07-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5f07-124">Library</span></span><br/> | <dl> <span data-ttu-id="b5f07-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5f07-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5f07-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5f07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f07-127">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b5f07-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

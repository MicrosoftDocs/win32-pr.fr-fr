---
description: 'D3DXMatrixDeterminant, fonction (D3DX10Math. h) : retourne le déterminant d’une matrice.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: D3DXMatrixDeterminant, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103457"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="a5630-103">D3DXMatrixDeterminant, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a5630-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="a5630-104">Retourne le déterminant d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="a5630-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5630-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5630-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a5630-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5630-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5630-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5630-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5630-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a5630-109">Pointeur vers la structure D3DXMATRIX source.</span><span class="sxs-lookup"><span data-stu-id="a5630-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5630-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5630-110">Return value</span></span>

<span data-ttu-id="a5630-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5630-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5630-112">Retourne le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a5630-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5630-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5630-113">Requirements</span></span>



| <span data-ttu-id="a5630-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5630-114">Requirement</span></span> | <span data-ttu-id="a5630-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5630-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5630-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5630-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a5630-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5630-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a5630-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5630-118">Library</span></span><br/> | <dl> <span data-ttu-id="a5630-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5630-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5630-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5630-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5630-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a5630-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

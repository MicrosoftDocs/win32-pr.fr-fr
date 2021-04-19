---
description: Retourne le déterminant d’une matrice.
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
ms.openlocfilehash: 11b1092427b12c33d8c34c9f1bbd5e09cf1ccf2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535837"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="08d01-103">D3DXMatrixDeterminant, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="08d01-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="08d01-104">Retourne le déterminant d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="08d01-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08d01-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="08d01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08d01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d01-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08d01-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d01-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="08d01-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="08d01-109">Pointeur vers la structure D3DXMATRIX source.</span><span class="sxs-lookup"><span data-stu-id="08d01-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d01-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08d01-110">Return value</span></span>

<span data-ttu-id="08d01-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08d01-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08d01-112">Retourne le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="08d01-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d01-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08d01-113">Requirements</span></span>



| <span data-ttu-id="08d01-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08d01-114">Requirement</span></span> | <span data-ttu-id="08d01-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08d01-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08d01-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="08d01-116">Header</span></span><br/>  | <dl> <span data-ttu-id="08d01-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d01-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="08d01-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08d01-118">Library</span></span><br/> | <dl> <span data-ttu-id="08d01-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08d01-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="08d01-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08d01-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d01-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="08d01-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

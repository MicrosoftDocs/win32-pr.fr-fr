---
description: 'D3DXMatrixDeterminant, fonction (D3dx9math. h) : retourne le déterminant d’une matrice.'
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: D3DXMatrixDeterminant, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098167"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="f23fa-103">D3DXMatrixDeterminant, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f23fa-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="f23fa-104">Retourne le déterminant d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="f23fa-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f23fa-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f23fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f23fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23fa-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f23fa-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f23fa-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f23fa-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f23fa-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="f23fa-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23fa-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f23fa-110">Return value</span></span>

<span data-ttu-id="f23fa-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f23fa-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f23fa-112">Retourne le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="f23fa-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23fa-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f23fa-113">Requirements</span></span>



| <span data-ttu-id="f23fa-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f23fa-114">Requirement</span></span> | <span data-ttu-id="f23fa-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f23fa-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f23fa-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="f23fa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f23fa-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23fa-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f23fa-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f23fa-118">Library</span></span><br/> | <dl> <span data-ttu-id="f23fa-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f23fa-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f23fa-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f23fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23fa-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f23fa-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

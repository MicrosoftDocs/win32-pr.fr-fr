---
description: Détermine si une matrice est une matrice d’identité.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: D3DXMatrixIsIdentity, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323150"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="26eb7-103">D3DXMatrixIsIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="26eb7-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="26eb7-104">Détermine si une matrice est une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="26eb7-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="26eb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26eb7-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="26eb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26eb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26eb7-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26eb7-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26eb7-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="26eb7-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26eb7-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui sera testée pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="26eb7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26eb7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26eb7-110">Return value</span></span>

<span data-ttu-id="26eb7-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26eb7-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26eb7-112">Si la matrice est une matrice d’identité, cette fonction retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="26eb7-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="26eb7-113">Dans le cas contraire, cette fonction retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="26eb7-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="26eb7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26eb7-114">Requirements</span></span>



| <span data-ttu-id="26eb7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26eb7-115">Requirement</span></span> | <span data-ttu-id="26eb7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="26eb7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26eb7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="26eb7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="26eb7-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26eb7-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="26eb7-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26eb7-119">Library</span></span><br/> | <dl> <span data-ttu-id="26eb7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26eb7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26eb7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26eb7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26eb7-122">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="26eb7-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="26eb7-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="26eb7-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 

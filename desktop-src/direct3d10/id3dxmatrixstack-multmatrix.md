---
description: 'ID3DXMATRIXStack :: MultMatrix, méthode (D3DX10. h)-détermine le produit de la matrice actuelle et la matrice donnée.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'ID3DXMATRIXStack :: MultMatrix, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107967"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="db68b-103">ID3DXMATRIXStack :: MultMatrix, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="db68b-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="db68b-104">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="db68b-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="db68b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db68b-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="db68b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db68b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db68b-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db68b-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db68b-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="db68b-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="db68b-109">Pointeur vers la structure D3DXMATRIX à multiplier avec la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="db68b-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db68b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db68b-110">Return value</span></span>

<span data-ttu-id="db68b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db68b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db68b-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db68b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db68b-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db68b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db68b-114">Notes </span><span class="sxs-lookup"><span data-stu-id="db68b-114">Remarks</span></span>

<span data-ttu-id="db68b-115">Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="db68b-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="db68b-116">Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice actuelle et la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="db68b-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="db68b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db68b-117">Requirements</span></span>



| <span data-ttu-id="db68b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db68b-118">Requirement</span></span> | <span data-ttu-id="db68b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="db68b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db68b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="db68b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="db68b-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="db68b-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="db68b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db68b-122">Library</span></span><br/> | <dl> <span data-ttu-id="db68b-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db68b-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db68b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db68b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db68b-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="db68b-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="db68b-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="db68b-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

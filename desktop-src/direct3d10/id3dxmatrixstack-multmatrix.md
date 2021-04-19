---
description: Détermine le produit de la matrice actuelle et de la matrice donnée.
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
ms.openlocfilehash: 43f80ca26f615e02570f0855b1ba6c2435e11b5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542199"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="d9a53-103">ID3DXMATRIXStack :: MultMatrix, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d9a53-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="d9a53-104">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="d9a53-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9a53-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d9a53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a53-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9a53-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a53-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d9a53-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9a53-109">Pointeur vers la structure D3DXMATRIX à multiplier avec la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="d9a53-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a53-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9a53-110">Return value</span></span>

<span data-ttu-id="d9a53-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9a53-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9a53-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9a53-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9a53-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d9a53-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a53-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d9a53-114">Remarks</span></span>

<span data-ttu-id="d9a53-115">Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="d9a53-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="d9a53-116">Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice actuelle et la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="d9a53-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a53-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9a53-117">Requirements</span></span>



| <span data-ttu-id="d9a53-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9a53-118">Requirement</span></span> | <span data-ttu-id="d9a53-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9a53-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a53-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9a53-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d9a53-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a53-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9a53-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9a53-122">Library</span></span><br/> | <dl> <span data-ttu-id="d9a53-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9a53-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a53-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9a53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a53-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d9a53-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d9a53-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d9a53-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

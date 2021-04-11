---
description: Détermine le produit de la matrice donnée et de la matrice actuelle.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'ID3DXMATRIXStack :: MultMatrixLocal, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211953"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="f8633-103">ID3DXMATRIXStack :: MultMatrixLocal, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f8633-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="f8633-104">Détermine le produit de la matrice donnée et de la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="f8633-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8633-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8633-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f8633-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8633-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8633-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8633-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8633-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8633-109">Pointeur vers la structure D3DXMATRIX à multiplier avec la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="f8633-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8633-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8633-110">Return value</span></span>

<span data-ttu-id="f8633-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8633-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8633-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8633-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8633-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8633-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8633-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f8633-114">Remarks</span></span>

<span data-ttu-id="f8633-115">Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine locale de l’objet).</span><span class="sxs-lookup"><span data-stu-id="f8633-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="f8633-116">Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice donnée et de la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="f8633-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8633-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8633-117">Requirements</span></span>



| <span data-ttu-id="f8633-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8633-118">Requirement</span></span> | <span data-ttu-id="f8633-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8633-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8633-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8633-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f8633-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8633-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8633-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8633-122">Library</span></span><br/> | <dl> <span data-ttu-id="f8633-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8633-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8633-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8633-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8633-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f8633-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f8633-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f8633-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

---
description: Détermine le produit de la matrice actuelle et de la matrice donnée.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack :: MultMatrix, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539431"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="ef3e6-103">ID3DXMATRIXStack :: MultMatrix, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ef3e6-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="ef3e6-104">Détermine le produit de la matrice actuelle et de la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="ef3e6-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef3e6-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="ef3e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef3e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef3e6-107">*pMat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef3e6-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3e6-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef3e6-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef3e6-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) à multiplier avec la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="ef3e6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef3e6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef3e6-110">Return value</span></span>

<span data-ttu-id="ef3e6-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef3e6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef3e6-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef3e6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef3e6-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ef3e6-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef3e6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ef3e6-114">Remarks</span></span>

<span data-ttu-id="ef3e6-115">Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="ef3e6-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="ef3e6-116">Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice actuelle et la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="ef3e6-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3e6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef3e6-117">Requirements</span></span>



| <span data-ttu-id="ef3e6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef3e6-118">Requirement</span></span> | <span data-ttu-id="ef3e6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef3e6-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3e6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef3e6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ef3e6-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef3e6-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ef3e6-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef3e6-122">Library</span></span><br/> | <dl> <span data-ttu-id="ef3e6-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef3e6-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef3e6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef3e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3e6-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ef3e6-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ef3e6-126">**ID3DXMATRIXStack::MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="ef3e6-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 





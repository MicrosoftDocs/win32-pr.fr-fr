---
description: Supprime la matrice actuelle du haut de la pile.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: ID3DXMATRIXStack ::P méthode op (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522395"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="8df0a-103">ID3DXMATRIXStack ::P méthode op (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="8df0a-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="8df0a-104">Supprime la matrice actuelle du haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8df0a-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8df0a-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="8df0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8df0a-106">Parameters</span></span>

<span data-ttu-id="8df0a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8df0a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8df0a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8df0a-108">Return value</span></span>

<span data-ttu-id="8df0a-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8df0a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8df0a-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8df0a-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df0a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8df0a-111">Remarks</span></span>

<span data-ttu-id="8df0a-112">Notez que cette méthode décrémente le nombre d’éléments sur la pile de 1, en supprimant efficacement la matrice actuelle du haut de la pile et en promouvant une matrice en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="8df0a-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="8df0a-113">Si le nombre actuel d’éléments sur la pile est 0, cette méthode retourne sans effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="8df0a-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="8df0a-114">Si le nombre actuel d’éléments sur la pile est 1, cette méthode vide la pile.</span><span class="sxs-lookup"><span data-stu-id="8df0a-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df0a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8df0a-115">Requirements</span></span>



| <span data-ttu-id="8df0a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8df0a-116">Requirement</span></span> | <span data-ttu-id="8df0a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8df0a-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8df0a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8df0a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8df0a-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df0a-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8df0a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8df0a-120">Library</span></span><br/> | <dl> <span data-ttu-id="8df0a-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df0a-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df0a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8df0a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df0a-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8df0a-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8df0a-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8df0a-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





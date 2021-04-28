---
description: ID3DXMATRIXStack ::P méthode op (D3DX10. h)-supprime la matrice actuelle du haut de la pile.
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
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107927"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="da8fe-103">ID3DXMATRIXStack ::P méthode op (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="da8fe-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="da8fe-104">Supprime la matrice actuelle du haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="da8fe-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="da8fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da8fe-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="da8fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da8fe-106">Parameters</span></span>

<span data-ttu-id="da8fe-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="da8fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da8fe-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da8fe-108">Return value</span></span>

<span data-ttu-id="da8fe-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da8fe-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da8fe-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da8fe-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8fe-111">Notes </span><span class="sxs-lookup"><span data-stu-id="da8fe-111">Remarks</span></span>

<span data-ttu-id="da8fe-112">Notez que cette méthode décrémente le nombre d’éléments sur la pile de 1, en supprimant efficacement la matrice actuelle du haut de la pile et en promouvant une matrice en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="da8fe-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="da8fe-113">Si le nombre actuel d’éléments sur la pile est 0, cette méthode retourne sans effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="da8fe-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="da8fe-114">Si le nombre actuel d’éléments sur la pile est 1, cette méthode vide la pile.</span><span class="sxs-lookup"><span data-stu-id="da8fe-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8fe-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da8fe-115">Requirements</span></span>



| <span data-ttu-id="da8fe-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da8fe-116">Requirement</span></span> | <span data-ttu-id="da8fe-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="da8fe-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da8fe-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="da8fe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="da8fe-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="da8fe-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="da8fe-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da8fe-120">Library</span></span><br/> | <dl> <span data-ttu-id="da8fe-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da8fe-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8fe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da8fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8fe-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="da8fe-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="da8fe-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="da8fe-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





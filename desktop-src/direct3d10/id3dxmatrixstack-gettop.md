---
description: Récupère la matrice actuelle en haut de la pile.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack :: GetTop, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535211"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="7c0eb-103">ID3DXMATRIXStack :: GetTop, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="7c0eb-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="7c0eb-104">Récupère la matrice actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="7c0eb-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c0eb-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="7c0eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c0eb-106">Parameters</span></span>

<span data-ttu-id="7c0eb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c0eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c0eb-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c0eb-108">Return value</span></span>

<span data-ttu-id="7c0eb-109">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c0eb-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c0eb-110">Cette méthode retourne un pointeur vers une structure D3DXMATRIX représentant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c0eb-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0eb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7c0eb-111">Remarks</span></span>

<span data-ttu-id="7c0eb-112">Il n’est pas garanti que le pointeur D3DXMATRIX retourné par cette méthode soit valide après les opérations de pile suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c0eb-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="7c0eb-113">Notez que cette méthode ne supprime pas la matrice actuelle du haut de la pile ; au lieu de cela, elle retourne simplement la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c0eb-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0eb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c0eb-114">Requirements</span></span>



| <span data-ttu-id="7c0eb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c0eb-115">Requirement</span></span> | <span data-ttu-id="7c0eb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c0eb-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0eb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c0eb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c0eb-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0eb-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c0eb-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c0eb-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c0eb-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c0eb-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0eb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c0eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0eb-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="7c0eb-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7c0eb-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7c0eb-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

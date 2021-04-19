---
description: Récupère la matrice actuelle en haut de la pile.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack :: GetTop, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523810"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="2db58-103">ID3DXMATRIXStack :: GetTop, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2db58-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="2db58-104">Récupère la matrice actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="2db58-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2db58-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="2db58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2db58-106">Parameters</span></span>

<span data-ttu-id="2db58-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2db58-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2db58-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2db58-108">Return value</span></span>

<span data-ttu-id="2db58-109">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2db58-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2db58-110">Cette méthode retourne un pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="2db58-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db58-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2db58-111">Remarks</span></span>

<span data-ttu-id="2db58-112">Il n’est pas garanti que le pointeur [**D3DXMATRIX**](d3dxmatrix.md) retourné par cette méthode soit valide après les opérations de pile suivantes.</span><span class="sxs-lookup"><span data-stu-id="2db58-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="2db58-113">Notez que cette méthode ne supprime pas la matrice actuelle du haut de la pile ; au lieu de cela, elle retourne simplement la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="2db58-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db58-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2db58-114">Requirements</span></span>



| <span data-ttu-id="2db58-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2db58-115">Requirement</span></span> | <span data-ttu-id="2db58-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2db58-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db58-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2db58-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2db58-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db58-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2db58-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2db58-119">Library</span></span><br/> | <dl> <span data-ttu-id="2db58-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db58-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2db58-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2db58-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db58-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2db58-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2db58-123">**ID3DXMATRIXStack ::P op**</span><span class="sxs-lookup"><span data-stu-id="2db58-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="2db58-124">**ID3DXMATRIXStack ::P par émission**</span><span class="sxs-lookup"><span data-stu-id="2db58-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 





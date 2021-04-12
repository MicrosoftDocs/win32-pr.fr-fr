---
description: Cette interface encapsule les fonctionnalités minimales requises d’une animation définie par un contrôleur d’animation.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interface ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211945"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="e61db-103">Interface ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e61db-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="e61db-104">Cette interface encapsule les fonctionnalités minimales requises d’une animation définie par un contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="e61db-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="e61db-105">Les utilisateurs expérimentés peuvent souhaiter implémenter cette interface eux-mêmes pour répondre à leurs besoins spécifiques. pour la plupart des utilisateurs, toutefois, les interfaces [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) et [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) dérivées devraient suffire.</span><span class="sxs-lookup"><span data-stu-id="e61db-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="e61db-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e61db-106">Members</span></span>

<span data-ttu-id="e61db-107">L’interface **ID3DXAnimationSet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e61db-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e61db-108">**ID3DXAnimationSet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e61db-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="e61db-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e61db-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e61db-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e61db-110">Methods</span></span>

<span data-ttu-id="e61db-111">L’interface **ID3DXAnimationSet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e61db-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="e61db-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="e61db-112">Method</span></span>                                                                        | <span data-ttu-id="e61db-113">Description</span><span class="sxs-lookup"><span data-stu-id="e61db-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="e61db-114">**GetAnimationIndexByName**</span><span class="sxs-lookup"><span data-stu-id="e61db-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="e61db-115">Obtient l’index d’une animation, en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="e61db-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="e61db-116">**GetAnimationNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="e61db-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="e61db-117">Obtient le nom d’une animation, en fonction de son index.</span><span class="sxs-lookup"><span data-stu-id="e61db-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="e61db-118">**GetCallback**</span><span class="sxs-lookup"><span data-stu-id="e61db-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="e61db-119">Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="e61db-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="e61db-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="e61db-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="e61db-121">Obtient le nom du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="e61db-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="e61db-122">**GetNumAnimations**</span><span class="sxs-lookup"><span data-stu-id="e61db-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="e61db-123">Obtient le nombre d’animations dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="e61db-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="e61db-124">**GetPeriod**</span><span class="sxs-lookup"><span data-stu-id="e61db-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="e61db-125">Obtient la période de l’animation définie.</span><span class="sxs-lookup"><span data-stu-id="e61db-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="e61db-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="e61db-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="e61db-127">Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="e61db-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="e61db-128">**GetSRT**</span><span class="sxs-lookup"><span data-stu-id="e61db-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="e61db-129">Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="e61db-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e61db-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e61db-130">Remarks</span></span>

<span data-ttu-id="e61db-131">Un jeu d’animations se compose d’animations pour de nombreux nœuds pour la même animation.</span><span class="sxs-lookup"><span data-stu-id="e61db-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="e61db-132">Le type LPD3DXANIMATIONSET est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="e61db-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="e61db-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e61db-133">Requirements</span></span>



| <span data-ttu-id="e61db-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e61db-134">Requirement</span></span> | <span data-ttu-id="e61db-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="e61db-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e61db-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="e61db-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e61db-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e61db-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e61db-138">Library</span></span><br/> | <dl> <span data-ttu-id="e61db-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e61db-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e61db-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61db-141">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e61db-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

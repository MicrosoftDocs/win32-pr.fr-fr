---
description: Obtient la période de l’animation définie.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet :: GetPeriod, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545895"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="c1c90-103">ID3DXAnimationSet :: GetPeriod, méthode</span><span class="sxs-lookup"><span data-stu-id="c1c90-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="c1c90-104">Obtient la période de l’animation définie.</span><span class="sxs-lookup"><span data-stu-id="c1c90-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1c90-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="c1c90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1c90-106">Parameters</span></span>

<span data-ttu-id="c1c90-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c1c90-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1c90-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1c90-108">Return value</span></span>

<span data-ttu-id="c1c90-109">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1c90-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1c90-110">Période de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c1c90-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c90-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c1c90-111">Remarks</span></span>

<span data-ttu-id="c1c90-112">La période est la plage de temps pendant laquelle les images clés d’animation sont valides.</span><span class="sxs-lookup"><span data-stu-id="c1c90-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="c1c90-113">Pour les animations de boucle, il s’agit de la période de la boucle.</span><span class="sxs-lookup"><span data-stu-id="c1c90-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="c1c90-114">Les unités de temps dans lesquelles les images clés sont spécifiées (par exemple, secondes) sont déterminées par l’application.</span><span class="sxs-lookup"><span data-stu-id="c1c90-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c90-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1c90-115">Requirements</span></span>



| <span data-ttu-id="c1c90-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1c90-116">Requirement</span></span> | <span data-ttu-id="c1c90-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1c90-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c90-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1c90-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c1c90-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c90-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c1c90-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1c90-120">Library</span></span><br/> | <dl> <span data-ttu-id="c1c90-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1c90-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1c90-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1c90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c90-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c1c90-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 

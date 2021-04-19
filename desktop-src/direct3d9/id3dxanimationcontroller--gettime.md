---
description: Obtient l’heure globale de l’animation.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController :: GetTime, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535826"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="ac70a-103">ID3DXAnimationController :: GetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="ac70a-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="ac70a-104">Obtient l’heure globale de l’animation.</span><span class="sxs-lookup"><span data-stu-id="ac70a-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac70a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac70a-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="ac70a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac70a-106">Parameters</span></span>

<span data-ttu-id="ac70a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac70a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac70a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac70a-108">Return value</span></span>

<span data-ttu-id="ac70a-109">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac70a-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac70a-110">Retourne l’heure globale de l’animation.</span><span class="sxs-lookup"><span data-stu-id="ac70a-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac70a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ac70a-111">Remarks</span></span>

<span data-ttu-id="ac70a-112">Les animations sont conçues à l’aide d’une heure d’animation locale et sont mélangées dans l’heure globale avec [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="ac70a-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac70a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac70a-113">Requirements</span></span>



| <span data-ttu-id="ac70a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac70a-114">Requirement</span></span> | <span data-ttu-id="ac70a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac70a-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac70a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac70a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ac70a-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac70a-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ac70a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac70a-118">Library</span></span><br/> | <dl> <span data-ttu-id="ac70a-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac70a-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac70a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac70a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac70a-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ac70a-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

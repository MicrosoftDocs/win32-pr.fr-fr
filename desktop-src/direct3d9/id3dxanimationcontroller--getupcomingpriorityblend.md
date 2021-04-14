---
description: Retourne un handle d’événement pour l’événement de fusion Priority suivant planifié pour se produire après un événement spécifié.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController :: GetUpcomingPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394055"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="777c1-103">ID3DXAnimationController :: GetUpcomingPriorityBlend, méthode</span><span class="sxs-lookup"><span data-stu-id="777c1-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="777c1-104">Retourne un handle d’événement pour l’événement de fusion Priority suivant planifié pour se produire après un événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="777c1-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="777c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="777c1-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="777c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="777c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777c1-107">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="777c1-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="777c1-108">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="777c1-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="777c1-109">Handle d’événement vers un événement spécifié après lequel Rechercher un événement de fusion de priorité suivant.</span><span class="sxs-lookup"><span data-stu-id="777c1-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="777c1-110">Si la valeur est **null**, la méthode retourne l’événement de fusion de la priorité planifiée suivante.</span><span class="sxs-lookup"><span data-stu-id="777c1-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777c1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="777c1-111">Return value</span></span>

<span data-ttu-id="777c1-112">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="777c1-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="777c1-113">Handle d’événement vers l’événement suivant de fusion de priorité planifiée.</span><span class="sxs-lookup"><span data-stu-id="777c1-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="777c1-114">La **valeur null** est retournée si aucun nouvel événement Priority Blend n’est planifié.</span><span class="sxs-lookup"><span data-stu-id="777c1-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="777c1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="777c1-115">Remarks</span></span>

<span data-ttu-id="777c1-116">Cette méthode peut être utilisée de façon itérative pour localiser un événement de fusion de priorité souhaité en passant à plusieurs reprises la **valeur null** pour hEvent.</span><span class="sxs-lookup"><span data-stu-id="777c1-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="777c1-117">N’effectuez pas d’itération après que la méthode a retourné la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="777c1-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="777c1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="777c1-118">Requirements</span></span>



| <span data-ttu-id="777c1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="777c1-119">Requirement</span></span> | <span data-ttu-id="777c1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="777c1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="777c1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="777c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="777c1-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="777c1-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="777c1-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="777c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="777c1-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="777c1-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="777c1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="777c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="777c1-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="777c1-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 





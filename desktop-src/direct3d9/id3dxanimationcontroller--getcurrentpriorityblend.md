---
description: Retourne un handle d’événement pour un événement de fusion de priorité en cours d’exécution.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'ID3DXAnimationController :: GetCurrentPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323294"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="d22de-103">ID3DXAnimationController :: GetCurrentPriorityBlend, méthode</span><span class="sxs-lookup"><span data-stu-id="d22de-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="d22de-104">Retourne un handle d’événement pour un événement de fusion de priorité en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d22de-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d22de-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="d22de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d22de-106">Parameters</span></span>

<span data-ttu-id="d22de-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d22de-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d22de-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d22de-108">Return value</span></span>

<span data-ttu-id="d22de-109">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="d22de-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="d22de-110">Handle d’événement vers l’événement de fusion de priorité en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d22de-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="d22de-111">La **valeur null** est retournée si aucun événement de fusion de priorité n’est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d22de-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22de-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d22de-112">Requirements</span></span>



| <span data-ttu-id="d22de-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d22de-113">Requirement</span></span> | <span data-ttu-id="d22de-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d22de-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d22de-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="d22de-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d22de-116"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22de-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d22de-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d22de-117">Library</span></span><br/> | <dl> <span data-ttu-id="d22de-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d22de-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d22de-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d22de-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22de-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d22de-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 





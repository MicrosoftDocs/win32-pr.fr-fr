---
description: Retourne un handle d’événement pour l’événement en cours d’exécution sur la piste d’animation spécifiée.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController :: GetCurrentTrackEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539903"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="f1a0d-103">ID3DXAnimationController :: GetCurrentTrackEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="f1a0d-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="f1a0d-104">Retourne un handle d’événement pour l’événement en cours d’exécution sur la piste d’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f1a0d-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1a0d-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="f1a0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a0d-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1a0d-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a0d-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1a0d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1a0d-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="f1a0d-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f1a0d-110">*EventType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1a0d-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a0d-111">Type : **[ **D3DXEVENT \_**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="f1a0d-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="f1a0d-112">Type d’événement à interroger.</span><span class="sxs-lookup"><span data-stu-id="f1a0d-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1a0d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1a0d-113">Return value</span></span>

<span data-ttu-id="f1a0d-114">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f1a0d-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f1a0d-115">Handle d’événement de l’événement en cours d’exécution sur la piste spécifiée. La **valeur null** est retournée si aucun événement n’est en cours d’exécution sur la piste spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f1a0d-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a0d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1a0d-116">Requirements</span></span>



| <span data-ttu-id="f1a0d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1a0d-117">Requirement</span></span> | <span data-ttu-id="f1a0d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a0d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a0d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1a0d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f1a0d-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1a0d-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f1a0d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1a0d-121">Library</span></span><br/> | <dl> <span data-ttu-id="f1a0d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1a0d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1a0d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1a0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a0d-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f1a0d-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 

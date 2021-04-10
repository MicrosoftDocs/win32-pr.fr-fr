---
description: Contient des informations sur un événement du système de tablette.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Structure SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210821"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="7bc96-103">Structure des données d' \_ événement système \_</span><span class="sxs-lookup"><span data-stu-id="7bc96-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="7bc96-104">Contient des informations sur un événement du système de tablette.</span><span class="sxs-lookup"><span data-stu-id="7bc96-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bc96-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="7bc96-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7bc96-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bc96-107">**bModifier**</span><span class="sxs-lookup"><span data-stu-id="7bc96-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-108">Valeurs de bit pour les modificateurs.</span><span class="sxs-lookup"><span data-stu-id="7bc96-108">Bit values for the modifiers.</span></span> <span data-ttu-id="7bc96-109">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7bc96-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="7bc96-110">**wKey**</span><span class="sxs-lookup"><span data-stu-id="7bc96-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-111">Analyser le code du caractère de clavier.</span><span class="sxs-lookup"><span data-stu-id="7bc96-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="7bc96-112">**xPos**</span><span class="sxs-lookup"><span data-stu-id="7bc96-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-113">Position X de l’événement.</span><span class="sxs-lookup"><span data-stu-id="7bc96-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="7bc96-114">**PosY**</span><span class="sxs-lookup"><span data-stu-id="7bc96-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-115">Position Y de l’événement.</span><span class="sxs-lookup"><span data-stu-id="7bc96-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="7bc96-116">**bCursorMode**</span><span class="sxs-lookup"><span data-stu-id="7bc96-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-117">Type de curseur qui a provoqué l’événement.</span><span class="sxs-lookup"><span data-stu-id="7bc96-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="7bc96-118">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7bc96-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="7bc96-119">**dwButtonState**</span><span class="sxs-lookup"><span data-stu-id="7bc96-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="7bc96-120">État des boutons au moment de l’événement système.</span><span class="sxs-lookup"><span data-stu-id="7bc96-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bc96-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7bc96-121">Remarks</span></span>

<span data-ttu-id="7bc96-122">Les événements système suivants sont définis pour être utilisés dans le membre **bModifier** .</span><span class="sxs-lookup"><span data-stu-id="7bc96-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="7bc96-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc96-123">Value</span></span>               | <span data-ttu-id="7bc96-124">Description</span><span class="sxs-lookup"><span data-stu-id="7bc96-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="7bc96-125">\_modificateur de se \_ CTRL</span><span class="sxs-lookup"><span data-stu-id="7bc96-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="7bc96-126">La touche de contrôle a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7bc96-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="7bc96-127">\_modificateur de se \_ ALT</span><span class="sxs-lookup"><span data-stu-id="7bc96-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="7bc96-128">La touche Alt a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7bc96-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="7bc96-129">\_changement de modificateur de se \_</span><span class="sxs-lookup"><span data-stu-id="7bc96-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="7bc96-130">La touche Maj a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7bc96-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="7bc96-131">Les événements système suivants sont définis pour être utilisés dans le membre **bCursorMode** .</span><span class="sxs-lookup"><span data-stu-id="7bc96-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="7bc96-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc96-132">Value</span></span>              | <span data-ttu-id="7bc96-133">Description</span><span class="sxs-lookup"><span data-stu-id="7bc96-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="7bc96-134">\_curseur normal \_ se</span><span class="sxs-lookup"><span data-stu-id="7bc96-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="7bc96-135">Indique l’info-bulle du stylet.</span><span class="sxs-lookup"><span data-stu-id="7bc96-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="7bc96-136">curseur de la \_ gomme se \_</span><span class="sxs-lookup"><span data-stu-id="7bc96-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="7bc96-137">Indique la gomme du stylet.</span><span class="sxs-lookup"><span data-stu-id="7bc96-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7bc96-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bc96-138">Requirements</span></span>



| <span data-ttu-id="7bc96-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bc96-139">Requirement</span></span> | <span data-ttu-id="7bc96-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc96-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7bc96-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc96-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc96-142">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bc96-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7bc96-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc96-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc96-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc96-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="7bc96-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bc96-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc96-146">**IStylusPlugin :: SystemEvent, méthode**</span><span class="sxs-lookup"><span data-stu-id="7bc96-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="7bc96-147">**ITabletEventSink :: SystemEvent, méthode**</span><span class="sxs-lookup"><span data-stu-id="7bc96-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 





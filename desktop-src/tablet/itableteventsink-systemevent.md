---
description: Se produit lorsqu’un événement système est disponible.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'ITabletEventSink :: SystemEvent, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523301"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="7ffd7-103">ITabletEventSink :: SystemEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="7ffd7-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="7ffd7-104">Se produit lorsqu’un événement système est disponible.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffd7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ffd7-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="7ffd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ffd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffd7-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ffd7-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffd7-108">Identificateur de la tablette.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="7ffd7-109">*CID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ffd7-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffd7-110">Identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="7ffd7-111">*événement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ffd7-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffd7-112">Code de l’événement système.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="7ffd7-113">*EventData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ffd7-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffd7-114">Données d’événement système.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffd7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ffd7-115">Return value</span></span>

<span data-ttu-id="7ffd7-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7ffd7-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7ffd7-117">Return code</span></span>                                                                            | <span data-ttu-id="7ffd7-118">Description</span><span class="sxs-lookup"><span data-stu-id="7ffd7-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7ffd7-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ffd7-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7ffd7-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7ffd7-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7ffd7-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7ffd7-122">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ffd7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7ffd7-123">Remarks</span></span>

<span data-ttu-id="7ffd7-124">La liste suivante contient les valeurs valides pour le paramètre d’événement.</span><span class="sxs-lookup"><span data-stu-id="7ffd7-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="7ffd7-125">\_appui sur se</span><span class="sxs-lookup"><span data-stu-id="7ffd7-125">SE\_TAP</span></span>
-   <span data-ttu-id="7ffd7-126">SE \_ double \_ Tap</span><span class="sxs-lookup"><span data-stu-id="7ffd7-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="7ffd7-127">clic \_ droit \_ sur</span><span class="sxs-lookup"><span data-stu-id="7ffd7-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="7ffd7-128">SE \_ faire glisser</span><span class="sxs-lookup"><span data-stu-id="7ffd7-128">SE\_DRAG</span></span>
-   <span data-ttu-id="7ffd7-129">SE \_ déplacer vers la droite \_</span><span class="sxs-lookup"><span data-stu-id="7ffd7-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="7ffd7-130">\_Appuyez sur \_ entrée</span><span class="sxs-lookup"><span data-stu-id="7ffd7-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="7ffd7-131">maintien de la \_ \_ sortie</span><span class="sxs-lookup"><span data-stu-id="7ffd7-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="7ffd7-132">\_point de suspension de la se \_</span><span class="sxs-lookup"><span data-stu-id="7ffd7-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="7ffd7-133">\_point de suspension de se \_</span><span class="sxs-lookup"><span data-stu-id="7ffd7-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="7ffd7-134">\_clic central \_ se</span><span class="sxs-lookup"><span data-stu-id="7ffd7-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="7ffd7-135">\_touche se</span><span class="sxs-lookup"><span data-stu-id="7ffd7-135">SE\_KEY</span></span>
-   <span data-ttu-id="7ffd7-136">\_touche de modification \_ se</span><span class="sxs-lookup"><span data-stu-id="7ffd7-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="7ffd7-137">\_mode de mouvement de se \_</span><span class="sxs-lookup"><span data-stu-id="7ffd7-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="7ffd7-138">\_curseur se</span><span class="sxs-lookup"><span data-stu-id="7ffd7-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffd7-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ffd7-139">Requirements</span></span>



| <span data-ttu-id="7ffd7-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ffd7-140">Requirement</span></span> | <span data-ttu-id="7ffd7-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ffd7-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffd7-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ffd7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffd7-143">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ffd7-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7ffd7-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ffd7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffd7-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ffd7-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7ffd7-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ffd7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ffd7-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ffd7-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffd7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ffd7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffd7-149">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="7ffd7-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 





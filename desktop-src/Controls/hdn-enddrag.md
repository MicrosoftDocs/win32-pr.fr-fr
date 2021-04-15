---
title: HDN_ENDDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle header lorsqu’une opération glisser est terminée sur l’un de ses éléments. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify. Seuls les contrôles d’en-tête définis sur le \_ style HDS DRAGDROP envoient ce code de notification.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- Contrôles Windows de code de notification HDN_ENDDRAG
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479453"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="a395d-106">\_Code de notification HDN ENDDRAG</span><span class="sxs-lookup"><span data-stu-id="a395d-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="a395d-107">Envoyé par un contrôle header lorsqu’une opération glisser est terminée sur l’un de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="a395d-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="a395d-108">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a395d-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="a395d-109">Seuls les contrôles d’en-tête définis sur le style [**HDS \_ DRAGDROP**](header-control-styles.md) envoient ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="a395d-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a395d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a395d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a395d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a395d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a395d-112">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenant des informations sur l’élément d’en-tête qui a été glissé.</span><span class="sxs-lookup"><span data-stu-id="a395d-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a395d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a395d-113">Return value</span></span>

<span data-ttu-id="a395d-114">Pour permettre au contrôle de placer et de réorganiser automatiquement l’élément, retournez **false**.</span><span class="sxs-lookup"><span data-stu-id="a395d-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="a395d-115">Pour empêcher l’élément d’être placé, retournez la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a395d-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a395d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a395d-116">Remarks</span></span>

<span data-ttu-id="a395d-117">Si le propriétaire effectue une gestion par glisser-déplacer externe (manuelle), il doit retourner la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="a395d-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="a395d-118">Le propriétaire doit ensuite réorganiser manuellement les éléments d’en-tête en envoyant [**HDM \_ SETITEM**](hdm-setitem.md) ou [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).</span><span class="sxs-lookup"><span data-stu-id="a395d-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a395d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a395d-119">Requirements</span></span>



| <span data-ttu-id="a395d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a395d-120">Requirement</span></span> | <span data-ttu-id="a395d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a395d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a395d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a395d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a395d-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a395d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a395d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a395d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a395d-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a395d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a395d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a395d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a395d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a395d-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






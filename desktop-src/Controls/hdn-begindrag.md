---
title: HDN_BEGINDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle header lorsqu’une opération glisser a commencé sur l’un de ses éléments. Ce code de notification est uniquement envoyé par les contrôles Header définis sur le \_ style HDS DRAGDROP. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Contrôles Windows de code de notification HDN_BEGINDRAG
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032792"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="e1c59-106">\_Code de notification HDN BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="e1c59-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="e1c59-107">Envoyé par un contrôle header lorsqu’une opération glisser a commencé sur l’un de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="e1c59-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="e1c59-108">Ce code de notification est uniquement envoyé par les contrôles Header définis sur le style [**HDS \_ DRAGDROP**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c59-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="e1c59-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c59-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e1c59-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1c59-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c59-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1c59-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1c59-112">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenant des informations sur l’élément d’en-tête qui est glissé.</span><span class="sxs-lookup"><span data-stu-id="e1c59-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c59-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1c59-113">Return value</span></span>

<span data-ttu-id="e1c59-114">Pour permettre au contrôle header de gérer automatiquement les opérations de glisser-déplacer, retournez **false**.</span><span class="sxs-lookup"><span data-stu-id="e1c59-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="e1c59-115">Si le propriétaire du contrôle effectue manuellement la réorganisation par glisser-déplacer, retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="e1c59-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c59-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e1c59-116">Remarks</span></span>

<span data-ttu-id="e1c59-117">Par défaut, un contrôle header gère automatiquement la réorganisation des opérations de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e1c59-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="e1c59-118">Le retour de la **valeur true** pour indiquer que la gestion du glisser-déplacer externe (manuelle) permet au propriétaire du contrôle de fournir des services personnalisés dans le cadre du processus de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e1c59-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c59-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1c59-119">Requirements</span></span>



| <span data-ttu-id="e1c59-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1c59-120">Requirement</span></span> | <span data-ttu-id="e1c59-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1c59-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c59-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1c59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1c59-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1c59-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1c59-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1c59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1c59-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1c59-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1c59-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1c59-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1c59-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1c59-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






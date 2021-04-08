---
title: Code de notification NM_LDOWN (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que le bouton gauche de la souris a été enfoncé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Contrôles Windows de code de notification NM_LDOWN (barre d’outils)
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843066"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="33e48-105">\_Code de notification LDOWN nm (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="33e48-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="33e48-106">Avertit la fenêtre parente d’une barre d’outils que le bouton gauche de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="33e48-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="33e48-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="33e48-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="33e48-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33e48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33e48-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33e48-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="33e48-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="33e48-111">Si l’utilisateur a cliqué sur un élément de la barre d’outils, le membre **dwItemSpec** contient l’identificateur de l’élément et le membre **dwItemData** contient les données de l’élément.</span><span class="sxs-lookup"><span data-stu-id="33e48-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="33e48-112">Si vous avez cliqué sur un séparateur ou un espace blanc dans la barre d’outils, le membre **dwItemSpec** contient-1.</span><span class="sxs-lookup"><span data-stu-id="33e48-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e48-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33e48-113">Return value</span></span>

<span data-ttu-id="33e48-114">Retourne **false** pour permettre au contrôle de barre d’outils d’effectuer le traitement par défaut de l’événement, ou **true** pour empêcher le contrôle de traiter l’événement.</span><span class="sxs-lookup"><span data-stu-id="33e48-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e48-115">Notes</span><span class="sxs-lookup"><span data-stu-id="33e48-115">Remarks</span></span>

<span data-ttu-id="33e48-116">Cette notification est envoyée après l’envoi du code de notification de [ \_ liste déroulante TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="33e48-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e48-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33e48-117">Requirements</span></span>



| <span data-ttu-id="33e48-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33e48-118">Requirement</span></span> | <span data-ttu-id="33e48-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="33e48-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33e48-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33e48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33e48-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33e48-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33e48-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33e48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33e48-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33e48-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33e48-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="33e48-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e48-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e48-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Code de notification NM_RCLICK (barre d’outils) (commctrl. h)
description: Envoyé par un contrôle ToolBar lorsque l’utilisateur clique sur la barre d’outils avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- Contrôles Windows de code de notification NM_RCLICK (barre d’outils)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516106"
---
# <a name="nm_rclick-toolbar-notification-code"></a><span data-ttu-id="1fe2a-105">\_Code de notification RCLICK nm (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="1fe2a-105">NM\_RCLICK (toolbar) notification code</span></span>

<span data-ttu-id="1fe2a-106">Envoyé par un contrôle ToolBar lorsque l’utilisateur clique sur la barre d’outils avec le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="1fe2a-106">Sent by a toolbar control when the user clicks the toolbar with the right mouse button.</span></span> <span data-ttu-id="1fe2a-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1fe2a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1fe2a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fe2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe2a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fe2a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fe2a-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="1fe2a-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="1fe2a-111">Si l’utilisateur a cliqué sur un élément de la barre d’outils, le membre **dwItemSpec** contient l’identificateur de l’élément et le membre **dwItemData** contient les données de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1fe2a-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="1fe2a-112">Si vous avez cliqué sur un séparateur ou un espace blanc dans la barre d’outils, le membre **dwItemSpec** contient-1.</span><span class="sxs-lookup"><span data-stu-id="1fe2a-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe2a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fe2a-113">Return value</span></span>

<span data-ttu-id="1fe2a-114">Retourne **false** pour permettre au contrôle de barre d’outils d’effectuer le traitement par défaut de l’événement, ou **true** pour empêcher le contrôle de traiter l’événement.</span><span class="sxs-lookup"><span data-stu-id="1fe2a-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe2a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fe2a-115">Requirements</span></span>



| <span data-ttu-id="1fe2a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fe2a-116">Requirement</span></span> | <span data-ttu-id="1fe2a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fe2a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe2a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fe2a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe2a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fe2a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fe2a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fe2a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe2a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fe2a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fe2a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fe2a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe2a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe2a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






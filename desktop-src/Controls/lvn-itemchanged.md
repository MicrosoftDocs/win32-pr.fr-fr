---
title: LVN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément a été modifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Contrôles Windows de code de notification LVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509761"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="18c73-105">\_Code de notification LVN ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="18c73-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="18c73-106">Avertit la fenêtre parente d’un contrôle List-View qu’un élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="18c73-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="18c73-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="18c73-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="18c73-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18c73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18c73-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18c73-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui identifie l’élément et spécifie quels attributs ont changé.</span><span class="sxs-lookup"><span data-stu-id="18c73-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="18c73-111">Si le membre **iItem** de la structure vers laquelle pointe *lParam* a la valeur-1, la modification a été appliquée à tous les éléments de la vue liste.</span><span class="sxs-lookup"><span data-stu-id="18c73-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18c73-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18c73-112">Return value</span></span>

<span data-ttu-id="18c73-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="18c73-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18c73-114">Notes</span><span class="sxs-lookup"><span data-stu-id="18c73-114">Remarks</span></span>

<span data-ttu-id="18c73-115">Si un contrôle d’affichage de liste a le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) et que l’utilisateur sélectionne une plage d’éléments en maintenant la touche Maj enfoncée et en cliquant sur la souris, les \_ codes de notification LVN ITEMCHANGED ne sont pas envoyés pour chaque élément sélectionné ou désélectionné.</span><span class="sxs-lookup"><span data-stu-id="18c73-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="18c73-116">Au lieu de cela, vous recevrez un code de notification [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) unique, indiquant que l’état d’une plage d’éléments a changé.</span><span class="sxs-lookup"><span data-stu-id="18c73-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c73-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18c73-117">Requirements</span></span>



| <span data-ttu-id="18c73-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18c73-118">Requirement</span></span> | <span data-ttu-id="18c73-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="18c73-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18c73-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c73-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18c73-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c73-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18c73-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c73-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18c73-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c73-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18c73-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="18c73-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18c73-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18c73-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






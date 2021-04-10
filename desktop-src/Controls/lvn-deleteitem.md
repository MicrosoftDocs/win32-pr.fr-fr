---
title: LVN_DELETEITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément est sur le point d’être supprimé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- Contrôles Windows de code de notification LVN_DELETEITEM
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106672"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="8e6da-105">\_Code de notification LVN DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="8e6da-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="8e6da-106">Avertit la fenêtre parente d’un contrôle List-View qu’un élément est sur le point d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="8e6da-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="8e6da-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e6da-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8e6da-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e6da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e6da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e6da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e6da-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="8e6da-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="8e6da-111">Le membre **iItem** identifie l’élément en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="8e6da-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="8e6da-112">Si le contrôle n’a pas le style **LVS \_ OWNERDATA** , *lParam* correspond aux données définies par l’application associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="8e6da-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="8e6da-113">Tous les autres membres de cette structure sont nuls.</span><span class="sxs-lookup"><span data-stu-id="8e6da-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e6da-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e6da-114">Return value</span></span>

<span data-ttu-id="8e6da-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8e6da-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e6da-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8e6da-116">Remarks</span></span>

<span data-ttu-id="8e6da-117">N’ajoutez pas, ne supprimez pas ou ne réorganisez pas les éléments en mode liste lors du traitement de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="8e6da-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e6da-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e6da-118">Requirements</span></span>



| <span data-ttu-id="8e6da-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e6da-119">Requirement</span></span> | <span data-ttu-id="8e6da-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e6da-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6da-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e6da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e6da-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e6da-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e6da-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e6da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e6da-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e6da-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e6da-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e6da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e6da-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e6da-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: TVN_SINGLEEXPAND le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View avec le \_ style TV SINGLEEXPAND style lorsque l’utilisateur ouvre ou ferme un élément d’arborescence en un seul clic de souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- Contrôles Windows de code de notification TVN_SINGLEEXPAND
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464659"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="733f3-105">\_Code de notification TVN SINGLEEXPAND</span><span class="sxs-lookup"><span data-stu-id="733f3-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="733f3-106">Envoyé par un contrôle Tree-View avec le style [**TV \_ SINGLEEXPAND**](tree-view-control-window-styles.md) style lorsque l’utilisateur ouvre ou ferme un élément d’arborescence en un seul clic de souris.</span><span class="sxs-lookup"><span data-stu-id="733f3-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="733f3-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="733f3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="733f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="733f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="733f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="733f3-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="733f3-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733f3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="733f3-111">Return value</span></span>

<span data-ttu-id="733f3-112">Return TVNRET \_ Default pour permettre au comportement par défaut de se produire.</span><span class="sxs-lookup"><span data-stu-id="733f3-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="733f3-113">Pour modifier le comportement par défaut, retournez :</span><span class="sxs-lookup"><span data-stu-id="733f3-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="733f3-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="733f3-114">Return code</span></span>                                                                                    | <span data-ttu-id="733f3-115">Description</span><span class="sxs-lookup"><span data-stu-id="733f3-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="733f3-116"><dt>**TVNRET \_ SKIPOLD**</dt></span><span class="sxs-lookup"><span data-stu-id="733f3-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="733f3-117">Ignore le traitement par défaut de l’élément non sélectionné.</span><span class="sxs-lookup"><span data-stu-id="733f3-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="733f3-118"><dt>**TVNRET \_ SKIPNEW**</dt></span><span class="sxs-lookup"><span data-stu-id="733f3-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="733f3-119">Ignorer le traitement par défaut de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="733f3-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="733f3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="733f3-120">Remarks</span></span>

<span data-ttu-id="733f3-121">Pour ignorer le traitement par défaut des éléments sélectionnés et désélectionnés, retournez TVNRET \_ SKIPOLD et TVNRET \_ SKIPNEW en les associant à un or logique.</span><span class="sxs-lookup"><span data-stu-id="733f3-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="733f3-122">Ce code de notification est uniquement envoyé par les contrôles d’arborescence avec le style [**TV \_ SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span><span class="sxs-lookup"><span data-stu-id="733f3-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="733f3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="733f3-123">Requirements</span></span>



| <span data-ttu-id="733f3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="733f3-124">Requirement</span></span> | <span data-ttu-id="733f3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="733f3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="733f3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="733f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="733f3-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="733f3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="733f3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="733f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="733f3-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="733f3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="733f3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="733f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="733f3-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="733f3-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






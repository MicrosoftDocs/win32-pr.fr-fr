---
title: LVN_COLUMNDROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque le bouton déroulant du mode liste est enfoncé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- Contrôles Windows de code de notification LVN_COLUMNDROPDOWN
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508582"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="f71bf-105">\_Code de notification LVN COLUMNDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="f71bf-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="f71bf-106">Envoyé par un contrôle List-View lorsque le bouton déroulant du mode liste est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="f71bf-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="f71bf-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f71bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f71bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f71bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71bf-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f71bf-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71bf-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui décrit le code de notification.</span><span class="sxs-lookup"><span data-stu-id="f71bf-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="f71bf-111">L’appelant est chargé d’allouer cette structure, y compris la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue.</span><span class="sxs-lookup"><span data-stu-id="f71bf-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="f71bf-112">Définissez les membres de la structure **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="f71bf-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="f71bf-113">Le membre de **code** doit être défini sur LVN \_ COLUMNDROPDOWN.</span><span class="sxs-lookup"><span data-stu-id="f71bf-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="f71bf-114">Affectez la valeur-1 au membre **iItem** de la structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="f71bf-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="f71bf-115">Définissez le membre **iSubItem** sur l’index du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="f71bf-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="f71bf-116">Définissez les membres **uNewState**, **uOldState** et **lParam** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f71bf-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="f71bf-117">Les membres restants de la structure **NMLISTVIEW** ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="f71bf-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71bf-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f71bf-118">Return value</span></span>

<span data-ttu-id="f71bf-119">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f71bf-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f71bf-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f71bf-120">Remarks</span></span>

<span data-ttu-id="f71bf-121">Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="f71bf-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="f71bf-122">Le paramètre *wParam* contient l’ID du contrôle qui envoie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="f71bf-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="f71bf-123">Si un contrôle header est un enfant de l’affichage de liste, le contrôle header doit envoyer ce code notifications au contrôle List-View lorsque le contrôle header reçoit le code de notification [ \_ DROPDOWN HDN](hdn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f71bf-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71bf-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f71bf-124">Requirements</span></span>



| <span data-ttu-id="f71bf-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f71bf-125">Requirement</span></span> | <span data-ttu-id="f71bf-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f71bf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f71bf-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f71bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f71bf-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f71bf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f71bf-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f71bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f71bf-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f71bf-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f71bf-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f71bf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71bf-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71bf-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






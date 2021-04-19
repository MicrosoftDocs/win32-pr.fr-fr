---
title: TVN_SETDISPINFO le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View qu’elle doit mettre à jour les informations qu’elle gère à propos d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- Contrôles Windows de code de notification TVN_SETDISPINFO
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518065"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="d06d7-105">\_Code de notification TVN SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d06d7-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="d06d7-106">Avertit la fenêtre parente d’un contrôle Tree-View qu’elle doit mettre à jour les informations qu’elle gère à propos d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d06d7-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="d06d7-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d06d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d06d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d06d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d06d7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d06d7-110">Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) qui décrit l’élément en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d06d7-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="d06d7-111">Le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) spécifie l’élément en cours de mise à jour et le membre **Mask** spécifie les attributs de l’élément à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="d06d7-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d06d7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d06d7-112">Return value</span></span>

<span data-ttu-id="d06d7-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d06d7-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d06d7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d06d7-114">Remarks</span></span>

<span data-ttu-id="d06d7-115">Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie cette notification pour définir le texte de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d06d7-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="d06d7-116">Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .</span><span class="sxs-lookup"><span data-stu-id="d06d7-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="d06d7-117">Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie cette notification pour récupérer l’index de l’image d’icône à afficher.</span><span class="sxs-lookup"><span data-stu-id="d06d7-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="d06d7-118">Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ image ou TVIF \_ SELECTEDIMAGE défini.</span><span class="sxs-lookup"><span data-stu-id="d06d7-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d06d7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d06d7-119">Requirements</span></span>



| <span data-ttu-id="d06d7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d06d7-120">Requirement</span></span> | <span data-ttu-id="d06d7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06d7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d06d7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d06d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d06d7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d06d7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d06d7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d06d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d06d7-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d06d7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d06d7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d06d7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d06d7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d06d7-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d06d7-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d06d7-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d06d7-129">**TVN \_ SETDISPINFOW** (Unicode) et **TVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d06d7-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d06d7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d06d7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06d7-131">**TVITEM**</span><span class="sxs-lookup"><span data-stu-id="d06d7-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="d06d7-132">**TVITEMEX**</span><span class="sxs-lookup"><span data-stu-id="d06d7-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="d06d7-133">TVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d06d7-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 






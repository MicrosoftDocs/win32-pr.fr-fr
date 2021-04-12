---
title: TVN_GETDISPINFO le code de notification (commctrl. h)
description: Demande qu’une fenêtre parente d’un contrôle Tree-View fournisse les informations nécessaires pour afficher ou trier un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Contrôles Windows de code de notification TVN_GETDISPINFO
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508609"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="d43b6-105">\_Code de notification TVN GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d43b6-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="d43b6-106">Demande qu’une fenêtre parente d’un contrôle Tree-View fournisse les informations nécessaires pour afficher ou trier un élément.</span><span class="sxs-lookup"><span data-stu-id="d43b6-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="d43b6-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d43b6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d43b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d43b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d43b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d43b6-110">Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d43b6-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="d43b6-111">Le membre de l' **élément** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **Mask**, **hitem**, **State** et **lParam** spécifient le type d’informations requis.</span><span class="sxs-lookup"><span data-stu-id="d43b6-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="d43b6-112">Vous devez remplir les membres de la structure avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="d43b6-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d43b6-113">Return value</span></span>

<span data-ttu-id="d43b6-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d43b6-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d43b6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d43b6-115">Remarks</span></span>

<span data-ttu-id="d43b6-116">Ce code de notification est envoyé dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="d43b6-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="d43b6-117">Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie ce code de notification pour récupérer le texte de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d43b6-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="d43b6-118">Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .</span><span class="sxs-lookup"><span data-stu-id="d43b6-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="d43b6-119">Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie ce code de notification pour récupérer l’index des icônes d’un élément dans la liste d’images du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d43b6-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="d43b6-120">Dans ce cas, si l’élément est sélectionné, l’indicateur TVIF SELECTEDIMAGE est défini pour le membre **Mask** de *lParam* \_ .</span><span class="sxs-lookup"><span data-stu-id="d43b6-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="d43b6-121">Si l’élément n’est pas sélectionné, l’indicateur d’image TVIF est défini pour le membre **Mask** de *lParam* \_ .</span><span class="sxs-lookup"><span data-stu-id="d43b6-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="d43b6-122">Si le membre **cChildren** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I CHILDRENCALLBACK, le contrôle envoie ce code de notification pour récupérer une valeur qui indique si l’élément a des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d43b6-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="d43b6-123">Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ Children Set.</span><span class="sxs-lookup"><span data-stu-id="d43b6-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43b6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d43b6-124">Requirements</span></span>



| <span data-ttu-id="d43b6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d43b6-125">Requirement</span></span> | <span data-ttu-id="d43b6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d43b6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d43b6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d43b6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d43b6-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d43b6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d43b6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d43b6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d43b6-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d43b6-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d43b6-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d43b6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d43b6-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d43b6-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d43b6-133">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d43b6-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d43b6-134">**TVN \_ GETDISPINFOW** (Unicode) et **TVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d43b6-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d43b6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d43b6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43b6-136">TVN \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d43b6-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 






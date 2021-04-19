---
title: LVN_INCREMENTALSEARCH le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’une recherche incrémentielle a démarré. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Contrôles Windows de code de notification LVN_INCREMENTALSEARCH
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513239"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="67f38-105">\_Code de notification LVN INCREMENTALSEARCH</span><span class="sxs-lookup"><span data-stu-id="67f38-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="67f38-106">Avertit la fenêtre parente d’un contrôle List-View qu’une recherche incrémentielle a démarré.</span><span class="sxs-lookup"><span data-stu-id="67f38-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="67f38-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f38-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="67f38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67f38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f38-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67f38-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f38-110">Pointeur vers une structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) qui décrit le code de notification.</span><span class="sxs-lookup"><span data-stu-id="67f38-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="67f38-111">L’appelant est chargé d’allouer cette structure, y compris les structures [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) et [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenues.</span><span class="sxs-lookup"><span data-stu-id="67f38-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="67f38-112">Définissez les membres de la structure **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="67f38-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="67f38-113">Le membre de **code** doit être défini sur LVN \_ INCREMENTALSEARCH.</span><span class="sxs-lookup"><span data-stu-id="67f38-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f38-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67f38-114">Return value</span></span>

<span data-ttu-id="67f38-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="67f38-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f38-116">Notes</span><span class="sxs-lookup"><span data-stu-id="67f38-116">Remarks</span></span>

<span data-ttu-id="67f38-117">Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="67f38-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="67f38-118">Le paramètre *wParam* contient l’ID du contrôle qui envoie ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="67f38-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="67f38-119">Ce code de notification donne à une application (ou au destinataire de notifications) la possibilité de personnaliser une recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="67f38-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="67f38-120">Par exemple, si les éléments de recherche sont numériques, l’application peut effectuer une recherche numérique au lieu d’une recherche de chaîne.</span><span class="sxs-lookup"><span data-stu-id="67f38-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="67f38-121">L’application définit le membre **lParam** de la structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenue dans la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sur le résultat de la recherche, ou sur une autre valeur définie par l’application pour faire échouer la recherche et indiquer au contrôle comment procéder.</span><span class="sxs-lookup"><span data-stu-id="67f38-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f38-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67f38-122">Requirements</span></span>



| <span data-ttu-id="67f38-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67f38-123">Requirement</span></span> | <span data-ttu-id="67f38-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f38-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f38-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f38-125">Minimum supported client</span></span><br/> | <span data-ttu-id="67f38-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f38-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67f38-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f38-127">Minimum supported server</span></span><br/> | <span data-ttu-id="67f38-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f38-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67f38-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="67f38-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f38-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67f38-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="67f38-131">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="67f38-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="67f38-132">**LVN \_ INCREMENTALSEARCHW** (Unicode) et **LVN \_ INCREMENTALSEARCHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="67f38-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 






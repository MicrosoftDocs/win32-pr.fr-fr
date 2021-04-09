---
title: LVN_GETEMPTYMARKUP le code de notification (commctrl. h)
description: Envoyé par le contrôle List-View à sa fenêtre parente lorsque le contrôle n’a pas d’éléments. Le \_ Code de notification LVN GETEMPTYMARKUP est une demande pour que la fenêtre parente fournisse du texte de balisage. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Contrôles Windows de code de notification LVN_GETEMPTYMARKUP
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844477"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="77d24-106">\_Code de notification LVN GETEMPTYMARKUP</span><span class="sxs-lookup"><span data-stu-id="77d24-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="77d24-107">Envoyé par le contrôle List-View à sa fenêtre parente lorsque le contrôle n’a pas d’éléments.</span><span class="sxs-lookup"><span data-stu-id="77d24-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="77d24-108">Le \_ Code de notification LVN GETEMPTYMARKUP est une demande pour que la fenêtre parente fournisse du texte de balisage.</span><span class="sxs-lookup"><span data-stu-id="77d24-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="77d24-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="77d24-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="77d24-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77d24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77d24-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77d24-112">Pointeur vers une structure [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="77d24-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="77d24-113">Définissez les membres de cette structure pour fournir le texte de balisage pour le contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="77d24-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d24-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77d24-114">Return value</span></span>

<span data-ttu-id="77d24-115">Retourne la **valeur true** pour définir le texte de balisage dans le contrôle d’affichage de liste, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77d24-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d24-116">Notes</span><span class="sxs-lookup"><span data-stu-id="77d24-116">Remarks</span></span>

<span data-ttu-id="77d24-117">Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="77d24-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="77d24-118">Le paramètre *wParam* contient l’ID du contrôle qui envoie ce message.</span><span class="sxs-lookup"><span data-stu-id="77d24-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d24-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77d24-119">Requirements</span></span>



| <span data-ttu-id="77d24-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77d24-120">Requirement</span></span> | <span data-ttu-id="77d24-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="77d24-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77d24-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77d24-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77d24-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77d24-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77d24-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77d24-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77d24-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77d24-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77d24-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="77d24-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d24-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d24-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






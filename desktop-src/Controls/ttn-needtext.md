---
title: TTN_NEEDTEXT le code de notification (commctrl. h)
description: Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle. Ce code de notification est identique à TTN \_ GETDISPINFO. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- Contrôles Windows de code de notification TTN_NEEDTEXT
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104425"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="c0718-106">\_Code de notification ttn NEEDTEXT</span><span class="sxs-lookup"><span data-stu-id="c0718-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="c0718-107">Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="c0718-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="c0718-108">Ce code de notification est identique à [ttn \_ GETDISPINFO](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="c0718-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="c0718-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c0718-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c0718-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0718-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0718-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0718-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0718-112">Pointeur vers une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) qui identifie l’outil qui a besoin du texte et reçoit les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="c0718-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0718-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0718-113">Return value</span></span>

<span data-ttu-id="c0718-114">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c0718-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0718-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c0718-115">Remarks</span></span>

<span data-ttu-id="c0718-116">Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="c0718-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="c0718-117">Si votre gestionnaire de messages définit le membre **uFlags** de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) sur ttf \_ di \_ SETITEM, le contrôle ToolTip stocke les informations et ne les redemande pas.</span><span class="sxs-lookup"><span data-stu-id="c0718-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0718-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0718-118">Requirements</span></span>



| <span data-ttu-id="c0718-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0718-119">Requirement</span></span> | <span data-ttu-id="c0718-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0718-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0718-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0718-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0718-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0718-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0718-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0718-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0718-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0718-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0718-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0718-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0718-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0718-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c0718-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c0718-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0718-128">**Ttn \_ NEEDTEXTW** (Unicode) et **ttn \_ NEEDTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c0718-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 






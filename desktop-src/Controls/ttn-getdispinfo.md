---
title: TTN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- Contrôles Windows de code de notification TTN_GETDISPINFO
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843881"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="7933c-105">\_Code de notification ttn GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="7933c-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="7933c-106">Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="7933c-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="7933c-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7933c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7933c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7933c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7933c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7933c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7933c-110">Pointeur vers une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) qui identifie l’outil qui a besoin du texte et reçoit les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="7933c-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7933c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7933c-111">Return value</span></span>

<span data-ttu-id="7933c-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7933c-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7933c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7933c-113">Remarks</span></span>

<span data-ttu-id="7933c-114">Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="7933c-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="7933c-115">Si votre gestionnaire de messages définit le membre **uFlags** de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) sur ttf \_ di \_ SETITEM, le contrôle ToolTip stocke les informations et ne les redemande pas.</span><span class="sxs-lookup"><span data-stu-id="7933c-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7933c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7933c-116">Requirements</span></span>



| <span data-ttu-id="7933c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7933c-117">Requirement</span></span> | <span data-ttu-id="7933c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7933c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7933c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7933c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7933c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7933c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7933c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7933c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7933c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7933c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7933c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7933c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7933c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7933c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7933c-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7933c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7933c-126">**Ttn \_ GETDISPINFOW** (Unicode) et **ttn \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7933c-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 






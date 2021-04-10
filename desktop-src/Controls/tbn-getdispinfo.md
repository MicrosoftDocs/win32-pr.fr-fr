---
title: TBN_GETDISPINFO le code de notification (commctrl. h)
description: Récupère les informations d’affichage d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Contrôles Windows de code de notification TBN_GETDISPINFO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105028"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="00f0d-105">\_Code de notification TBN GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="00f0d-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="00f0d-106">Récupère les informations d’affichage d’un élément de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="00f0d-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="00f0d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="00f0d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="00f0d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00f0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00f0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00f0d-110">Pointeur vers une structure [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="00f0d-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="00f0d-111">Le membre **idCommand** spécifie l’identificateur de commande de l’élément, le membre **lParam** contient les données définies par l’application de l’élément et le membre **dwMask** spécifie les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="00f0d-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f0d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00f0d-112">Return value</span></span>

<span data-ttu-id="00f0d-113">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="00f0d-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f0d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00f0d-114">Requirements</span></span>



| <span data-ttu-id="00f0d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00f0d-115">Requirement</span></span> | <span data-ttu-id="00f0d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="00f0d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00f0d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00f0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00f0d-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00f0d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00f0d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00f0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00f0d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00f0d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00f0d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="00f0d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f0d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f0d-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="00f0d-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="00f0d-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="00f0d-124">**TBN \_ GETDISPINFOW** (Unicode) et **TBN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="00f0d-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 






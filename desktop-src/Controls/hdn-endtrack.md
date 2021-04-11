---
title: HDN_ENDTRACK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a fini de faire glisser un séparateur. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- Contrôles Windows de code de notification HDN_ENDTRACK
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032434"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="874d4-105">\_Code de notification HDN ENDTRACK</span><span class="sxs-lookup"><span data-stu-id="874d4-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="874d4-106">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a fini de faire glisser un séparateur.</span><span class="sxs-lookup"><span data-stu-id="874d4-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="874d4-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="874d4-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="874d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="874d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="874d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="874d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="874d4-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément dont le séparateur a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="874d4-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="874d4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="874d4-111">Return value</span></span>

<span data-ttu-id="874d4-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="874d4-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="874d4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="874d4-113">Requirements</span></span>



| <span data-ttu-id="874d4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="874d4-114">Requirement</span></span> | <span data-ttu-id="874d4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="874d4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="874d4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="874d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="874d4-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="874d4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="874d4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="874d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="874d4-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="874d4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="874d4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="874d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="874d4-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="874d4-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="874d4-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="874d4-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="874d4-123">**HDN \_ ENDTRACKW** (Unicode) et **HDN \_ ENDTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="874d4-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 






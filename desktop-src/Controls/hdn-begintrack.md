---
title: HDN_BEGINTRACK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a commencé à faire glisser un séparateur dans le contrôle (autrement dit, l’utilisateur a appuyé sur le bouton gauche de la souris pendant que le curseur de la souris se trouve sur un séparateur dans le contrôle header).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- Contrôles Windows de code de notification HDN_BEGINTRACK
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106684"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="4eef3-104">\_Code de notification HDN BEGINTRACK</span><span class="sxs-lookup"><span data-stu-id="4eef3-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="4eef3-105">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a commencé à faire glisser un séparateur dans le contrôle (autrement dit, l’utilisateur a appuyé sur le bouton gauche de la souris pendant que le curseur de la souris se trouve sur un séparateur dans le contrôle header).</span><span class="sxs-lookup"><span data-stu-id="4eef3-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="4eef3-106">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4eef3-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4eef3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4eef3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eef3-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4eef3-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4eef3-109">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément dont le séparateur doit être glissé.</span><span class="sxs-lookup"><span data-stu-id="4eef3-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eef3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4eef3-110">Return value</span></span>

<span data-ttu-id="4eef3-111">Retourne **false** pour autoriser le suivi du séparateur, ou **true** pour empêcher le suivi.</span><span class="sxs-lookup"><span data-stu-id="4eef3-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eef3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4eef3-112">Requirements</span></span>



| <span data-ttu-id="4eef3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4eef3-113">Requirement</span></span> | <span data-ttu-id="4eef3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eef3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4eef3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eef3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4eef3-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4eef3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4eef3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eef3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4eef3-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4eef3-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4eef3-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4eef3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eef3-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eef3-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4eef3-121">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4eef3-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4eef3-122">**HDN \_ BEGINTRACKW** (Unicode) et **HDN \_ BEGINTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4eef3-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 






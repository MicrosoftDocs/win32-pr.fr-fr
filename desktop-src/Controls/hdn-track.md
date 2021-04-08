---
title: HDN_TRACK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur fait glisser un séparateur dans le contrôle header. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- Contrôles Windows de code de notification HDN_TRACK
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843890"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="0a8d5-105">\_Code de notification HDN Track</span><span class="sxs-lookup"><span data-stu-id="0a8d5-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="0a8d5-106">Avertit la fenêtre parente d’un contrôle header que l’utilisateur fait glisser un séparateur dans le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="0a8d5-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="0a8d5-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0a8d5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0a8d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a8d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a8d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a8d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a8d5-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément dont le séparateur est glissé.</span><span class="sxs-lookup"><span data-stu-id="0a8d5-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a8d5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a8d5-111">Return value</span></span>

<span data-ttu-id="0a8d5-112">Retourne **false** pour poursuivre le suivi du séparateur, ou **true** pour terminer le suivi.</span><span class="sxs-lookup"><span data-stu-id="0a8d5-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a8d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a8d5-113">Requirements</span></span>



| <span data-ttu-id="0a8d5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a8d5-114">Requirement</span></span> | <span data-ttu-id="0a8d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a8d5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8d5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a8d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a8d5-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a8d5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a8d5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a8d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a8d5-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a8d5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a8d5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a8d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a8d5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a8d5-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0a8d5-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="0a8d5-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0a8d5-123">**HDN \_ TRACKW** (Unicode) et **HDN \_ tracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0a8d5-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 






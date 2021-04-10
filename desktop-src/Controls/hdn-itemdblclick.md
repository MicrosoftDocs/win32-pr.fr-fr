---
title: HDN_ITEMDBLCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify. Seuls les contrôles d’en-tête définis sur le \_ style des boutons HDS envoient ce code de notification.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- Contrôles Windows de code de notification HDN_ITEMDBLCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200579"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="7bc41-106">\_Code de notification HDN ITEMDBLCLICK</span><span class="sxs-lookup"><span data-stu-id="7bc41-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="7bc41-107">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="7bc41-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="7bc41-108">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc41-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="7bc41-109">Seuls les contrôles d’en-tête définis sur le style des [**\_ boutons HDS**](header-control-styles.md) envoient ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="7bc41-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7bc41-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bc41-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc41-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bc41-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc41-112">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="7bc41-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bc41-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bc41-113">Return value</span></span>

<span data-ttu-id="7bc41-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7bc41-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc41-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bc41-115">Requirements</span></span>



| <span data-ttu-id="7bc41-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bc41-116">Requirement</span></span> | <span data-ttu-id="7bc41-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc41-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc41-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc41-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bc41-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7bc41-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc41-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bc41-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bc41-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bc41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bc41-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bc41-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7bc41-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7bc41-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7bc41-125">**HDN \_ ITEMDBLCLICKW** (Unicode) et **HDN \_ ITEMDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7bc41-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 






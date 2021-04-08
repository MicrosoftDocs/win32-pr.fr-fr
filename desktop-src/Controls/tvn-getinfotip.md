---
title: TVN_GETINFOTIP le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View qui a le style de l’info-bulle du téléviseur \_ . Ce code de notification est envoyé lorsque le contrôle demande des informations de texte supplémentaires à afficher dans une info-bulle. Le code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- Contrôles Windows de code de notification TVN_GETINFOTIP
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742253"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="bdd91-106">\_Code de notification TVN GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="bdd91-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="bdd91-107">Envoyé par un contrôle Tree-View qui a le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd91-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="bdd91-108">Ce code de notification est envoyé lorsque le contrôle demande des informations de texte supplémentaires à afficher dans une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="bdd91-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="bdd91-109">Le code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd91-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="bdd91-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdd91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd91-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdd91-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd91-112">Pointeur vers une structure [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="bdd91-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd91-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdd91-113">Return value</span></span>

<span data-ttu-id="bdd91-114">Le contrôle ignore la valeur de retour pour ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="bdd91-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd91-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bdd91-115">Remarks</span></span>

<span data-ttu-id="bdd91-116">Ce code de notification est uniquement envoyé par les contrôles d’arborescence qui ont le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd91-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd91-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdd91-117">Requirements</span></span>



| <span data-ttu-id="bdd91-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdd91-118">Requirement</span></span> | <span data-ttu-id="bdd91-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdd91-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd91-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdd91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd91-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdd91-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdd91-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdd91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd91-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdd91-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdd91-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdd91-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdd91-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdd91-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bdd91-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="bdd91-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bdd91-127">**TVN \_ GETINFOTIPW** (Unicode) et **TVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bdd91-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 






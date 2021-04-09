---
title: NM_SETCURSOR le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle définit le curseur en réponse à un \_ message WM SETCURSOR. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- Contrôles Windows de code de notification NM_SETCURSOR
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103349"
---
# <a name="nm_setcursor-notification-code"></a><span data-ttu-id="12c41-105">\_Code de notification SETCURSOR nm</span><span class="sxs-lookup"><span data-stu-id="12c41-105">NM\_SETCURSOR notification code</span></span>

<span data-ttu-id="12c41-106">Avertit la fenêtre parente d’un contrôle que le contrôle définit le curseur en réponse à un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="12c41-106">Notifies a control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="12c41-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="12c41-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="12c41-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12c41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12c41-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="12c41-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c41-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12c41-111">Return value</span></span>

<span data-ttu-id="12c41-112">Retournez zéro pour permettre au contrôle de définir le curseur ou une valeur différente de zéro pour empêcher le contrôle de définir le curseur.</span><span class="sxs-lookup"><span data-stu-id="12c41-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c41-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12c41-113">Requirements</span></span>



| <span data-ttu-id="12c41-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12c41-114">Requirement</span></span> | <span data-ttu-id="12c41-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="12c41-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12c41-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12c41-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c41-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12c41-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12c41-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c41-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12c41-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="12c41-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c41-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12c41-121"><dt>Commctrl.h</dt></span></span> </dl> |



 


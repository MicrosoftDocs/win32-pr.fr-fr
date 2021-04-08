---
title: TCN_FOCUSCHANGE le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que le focus du bouton a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- Contrôles Windows de code de notification TCN_FOCUSCHANGE
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739868"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="53531-105">\_Code de notification TCN FOCUSCHANGE</span><span class="sxs-lookup"><span data-stu-id="53531-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="53531-106">Avertit une fenêtre parente d’un contrôle onglet que le focus du bouton a changé.</span><span class="sxs-lookup"><span data-stu-id="53531-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="53531-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="53531-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="53531-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53531-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53531-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53531-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="53531-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53531-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53531-111">Return value</span></span>

<span data-ttu-id="53531-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="53531-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53531-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53531-113">Requirements</span></span>



| <span data-ttu-id="53531-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53531-114">Requirement</span></span> | <span data-ttu-id="53531-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="53531-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53531-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53531-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53531-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53531-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53531-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53531-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53531-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53531-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53531-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="53531-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53531-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53531-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






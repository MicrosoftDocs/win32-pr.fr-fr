---
title: NM_CLICK (onglet) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Contrôles Windows de code de notification NM_CLICK (onglet)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106639"
---
# <a name="nm_click-tab-notification-code"></a><span data-ttu-id="03597-105">\_Code de notification de clic (onglet) nm</span><span class="sxs-lookup"><span data-stu-id="03597-105">NM\_CLICK (tab) notification code</span></span>

<span data-ttu-id="03597-106">Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="03597-106">Notifies the parent window of a tab control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="03597-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="03597-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="03597-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03597-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03597-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03597-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03597-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="03597-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03597-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03597-111">Return value</span></span>

<span data-ttu-id="03597-112">La valeur de retour est ignorée par le contrôle Tab.</span><span class="sxs-lookup"><span data-stu-id="03597-112">The return value is ignored by the tab control.</span></span>

## <a name="requirements"></a><span data-ttu-id="03597-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03597-113">Requirements</span></span>



| <span data-ttu-id="03597-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03597-114">Requirement</span></span> | <span data-ttu-id="03597-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03597-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03597-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03597-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03597-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03597-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03597-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03597-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03597-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03597-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03597-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="03597-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03597-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03597-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






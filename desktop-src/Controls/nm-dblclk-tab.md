---
title: NM_DBLCLK (onglet) Code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Contrôles Windows de code de notification NM_DBLCLK (onglet)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105454"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="22e1e-105">\_Code de notification DBLCLK nm (onglet)</span><span class="sxs-lookup"><span data-stu-id="22e1e-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="22e1e-106">Avertit une fenêtre parente d’un contrôle onglet que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="22e1e-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="22e1e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="22e1e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="22e1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22e1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22e1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22e1e-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="22e1e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e1e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22e1e-111">Return value</span></span>

<span data-ttu-id="22e1e-112">Retourne une valeur différente de zéro pour ne pas autoriser le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="22e1e-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e1e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22e1e-113">Requirements</span></span>



| <span data-ttu-id="22e1e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22e1e-114">Requirement</span></span> | <span data-ttu-id="22e1e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="22e1e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22e1e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22e1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22e1e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22e1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22e1e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22e1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22e1e-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22e1e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22e1e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="22e1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22e1e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e1e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






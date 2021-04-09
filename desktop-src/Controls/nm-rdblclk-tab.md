---
title: NM_RDBLCLK (onglet) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a double-cliqué dans le contrôle avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- Contrôles Windows de code de notification NM_RDBLCLK (onglet)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032343"
---
# <a name="nm_rdblclk-tab-notification-code"></a><span data-ttu-id="07380-105">\_Code de notification RDBLCLK nm (onglet)</span><span class="sxs-lookup"><span data-stu-id="07380-105">NM\_RDBLCLK (tab) notification code</span></span>

<span data-ttu-id="07380-106">Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a double-cliqué dans le contrôle avec le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="07380-106">Notifies the parent window of a tab control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="07380-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07380-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="07380-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07380-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07380-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07380-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07380-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="07380-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07380-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07380-111">Return value</span></span>

<span data-ttu-id="07380-112">Retourne une valeur différente de zéro pour ne pas autoriser le traitement par défaut, ou zéro pour autoriser le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="07380-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="07380-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07380-113">Requirements</span></span>



| <span data-ttu-id="07380-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07380-114">Requirement</span></span> | <span data-ttu-id="07380-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="07380-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07380-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07380-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07380-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07380-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07380-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07380-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07380-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07380-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07380-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="07380-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07380-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07380-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Code de notification NM_RELEASEDCAPTURE (barre d’outils) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle ToolBar que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (barre d’outils)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d915b3af073ba0c6b5c74a7b13317f7b2d4ab8a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103909"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a><span data-ttu-id="ed3a5-105">\_Code de notification RELEASEDCAPTURE nm (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="ed3a5-105">NM\_RELEASEDCAPTURE (toolbar) notification code</span></span>

<span data-ttu-id="ed3a5-106">Avertit une fenêtre parente d’un contrôle ToolBar que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="ed3a5-106">Notifies a toolbar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="ed3a5-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ed3a5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ed3a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed3a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed3a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed3a5-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="ed3a5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3a5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed3a5-111">Return value</span></span>

<span data-ttu-id="ed3a5-112">Le contrôle ignore la valeur de retour de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="ed3a5-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed3a5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed3a5-113">Requirements</span></span>



| <span data-ttu-id="ed3a5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed3a5-114">Requirement</span></span> | <span data-ttu-id="ed3a5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed3a5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3a5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed3a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3a5-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed3a5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed3a5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed3a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3a5-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed3a5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed3a5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed3a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed3a5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed3a5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






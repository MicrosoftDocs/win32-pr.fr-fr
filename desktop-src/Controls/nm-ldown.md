---
title: NM_LDOWN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le bouton gauche de la souris a été enfoncé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- Contrôles Windows de code de notification NM_LDOWN
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518059"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="75c43-105">\_Code de notification LDOWN nm</span><span class="sxs-lookup"><span data-stu-id="75c43-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="75c43-106">Avertit la fenêtre parente d’un contrôle que le bouton gauche de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="75c43-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="75c43-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="75c43-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="75c43-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75c43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c43-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75c43-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75c43-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="75c43-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c43-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75c43-111">Return value</span></span>

<span data-ttu-id="75c43-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="75c43-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c43-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75c43-113">Requirements</span></span>



| <span data-ttu-id="75c43-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75c43-114">Requirement</span></span> | <span data-ttu-id="75c43-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="75c43-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75c43-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75c43-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75c43-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75c43-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75c43-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75c43-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75c43-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="75c43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75c43-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c43-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






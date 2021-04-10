---
title: NM_KILLFOCUS (date et heure) Code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- Contrôles Windows de code de notification NM_KILLFOCUS (date et heure)
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941664"
---
# <a name="nm_killfocus-date-time-notification-code"></a><span data-ttu-id="56394-105">\_KILLFOCUS nm (date et heure) Code de notification</span><span class="sxs-lookup"><span data-stu-id="56394-105">NM\_KILLFOCUS (date time) notification code</span></span>

<span data-ttu-id="56394-106">Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a perdu le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="56394-106">Notifies a date and time picker control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="56394-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="56394-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="56394-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56394-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56394-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56394-110">Adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="56394-110">The address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56394-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56394-111">Return value</span></span>

<span data-ttu-id="56394-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="56394-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="56394-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56394-113">Requirements</span></span>



| <span data-ttu-id="56394-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56394-114">Requirement</span></span> | <span data-ttu-id="56394-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="56394-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56394-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56394-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56394-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56394-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56394-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56394-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56394-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56394-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56394-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="56394-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56394-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56394-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






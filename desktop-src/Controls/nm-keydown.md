---
title: NM_KEYDOWN le code de notification (commctrl. h)
description: NM_KEYDOWN code de notification-envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- Contrôles Windows de code de notification NM_KEYDOWN
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112347"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="cfe2c-105">Code de notification de KeyOut NM \_</span><span class="sxs-lookup"><span data-stu-id="cfe2c-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="cfe2c-106">Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="cfe2c-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="cfe2c-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cfe2c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cfe2c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfe2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe2c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfe2c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe2c-110">Pointeur vers une structure [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) qui contient des informations supplémentaires sur la clé qui a provoqué le code de notification.</span><span class="sxs-lookup"><span data-stu-id="cfe2c-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe2c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cfe2c-111">Return value</span></span>

<span data-ttu-id="cfe2c-112">Retourne une valeur différente de zéro pour empêcher le contrôle de traiter la clé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cfe2c-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe2c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfe2c-113">Requirements</span></span>



| <span data-ttu-id="cfe2c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfe2c-114">Requirement</span></span> | <span data-ttu-id="cfe2c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfe2c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe2c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfe2c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe2c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfe2c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfe2c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfe2c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe2c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfe2c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfe2c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfe2c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe2c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe2c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






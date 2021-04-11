---
title: Code de notification NM_KEYDOWN (barre d’outils) (commctrl. h)
description: Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Contrôles Windows de code de notification NM_KEYDOWN (barre d’outils)
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
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032346"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="9ef08-105">\_Code de notification (barre d’outils) de la touche nm</span><span class="sxs-lookup"><span data-stu-id="9ef08-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="9ef08-106">Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="9ef08-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="9ef08-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef08-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9ef08-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ef08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef08-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ef08-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ef08-110">Pointeur vers une structure [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) qui contient des informations supplémentaires sur la clé qui a provoqué le code de notification.</span><span class="sxs-lookup"><span data-stu-id="9ef08-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef08-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ef08-111">Return value</span></span>

<span data-ttu-id="9ef08-112">Retourne une valeur différente de zéro pour empêcher le contrôle de traiter la clé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9ef08-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef08-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ef08-113">Remarks</span></span>

<span data-ttu-id="9ef08-114">Actuellement, seul le contrôle ToolBar envoie ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="9ef08-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef08-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ef08-115">Requirements</span></span>



| <span data-ttu-id="9ef08-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ef08-116">Requirement</span></span> | <span data-ttu-id="9ef08-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ef08-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef08-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ef08-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef08-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ef08-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ef08-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ef08-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef08-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ef08-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ef08-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ef08-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef08-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef08-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






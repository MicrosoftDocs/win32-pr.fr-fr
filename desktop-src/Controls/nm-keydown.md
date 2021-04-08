---
title: NM_KEYDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
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
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843070"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="bf869-105">Code de notification de KeyOut NM \_</span><span class="sxs-lookup"><span data-stu-id="bf869-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="bf869-106">Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="bf869-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="bf869-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf869-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bf869-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf869-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf869-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf869-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf869-110">Pointeur vers une structure [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) qui contient des informations supplémentaires sur la clé qui a provoqué le code de notification.</span><span class="sxs-lookup"><span data-stu-id="bf869-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf869-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf869-111">Return value</span></span>

<span data-ttu-id="bf869-112">Retourne une valeur différente de zéro pour empêcher le contrôle de traiter la clé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bf869-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf869-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf869-113">Requirements</span></span>



| <span data-ttu-id="bf869-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf869-114">Requirement</span></span> | <span data-ttu-id="bf869-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf869-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf869-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf869-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf869-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf869-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf869-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf869-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf869-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf869-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf869-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf869-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf869-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf869-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






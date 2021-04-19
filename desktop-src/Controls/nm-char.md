---
title: NM_CHAR le code de notification (commctrl. h)
description: Le code de notification de caractère NM \_ est envoyé par un contrôle lorsqu’une touche de caractère est traitée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- Contrôles Windows de code de notification NM_CHAR
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517339"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="a4887-105">\_Code de notification de caractère nm</span><span class="sxs-lookup"><span data-stu-id="a4887-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="a4887-106">Le code de notification de caractère NM \_ est envoyé par un contrôle lorsqu’une touche de caractère est traitée.</span><span class="sxs-lookup"><span data-stu-id="a4887-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="a4887-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a4887-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a4887-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4887-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4887-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4887-110">Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient des informations supplémentaires sur le caractère qui a provoqué le code de notification.</span><span class="sxs-lookup"><span data-stu-id="a4887-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4887-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4887-111">Return value</span></span>

<span data-ttu-id="a4887-112">La valeur de retour est ignorée par la plupart des contrôles.</span><span class="sxs-lookup"><span data-stu-id="a4887-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="a4887-113">Pour plus d’informations, consultez la documentation relative aux contrôles individuels.</span><span class="sxs-lookup"><span data-stu-id="a4887-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4887-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4887-114">Requirements</span></span>



| <span data-ttu-id="a4887-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4887-115">Requirement</span></span> | <span data-ttu-id="a4887-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4887-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4887-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4887-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4887-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4887-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4887-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4887-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4887-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4887-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4887-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4887-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4887-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4887-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4887-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4887-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4887-124">NM \_ caractère (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="a4887-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 






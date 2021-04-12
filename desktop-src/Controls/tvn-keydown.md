---
title: TVN_KEYDOWN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a appuyé sur une touche et que le contrôle Tree-View a le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- Contrôles Windows de code de notification TVN_KEYDOWN
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464246"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="e114f-105">Code de notification KeyOut TVN \_</span><span class="sxs-lookup"><span data-stu-id="e114f-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="e114f-106">Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a appuyé sur une touche et que le contrôle Tree-View a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e114f-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="e114f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e114f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="e114f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e114f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e114f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e114f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e114f-110">Pointeur vers une structure [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="e114f-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="e114f-111">Le membre **wVKey** spécifie le code de la touche virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e114f-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e114f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e114f-112">Return value</span></span>

<span data-ttu-id="e114f-113">Si le membre **wVKey** de *lParam* est un code de touche de caractères, le caractère sera utilisé dans le cadre d’une recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="e114f-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="e114f-114">Retourne une valeur différente de zéro pour exclure le caractère de la recherche incrémentielle, ou zéro pour inclure le caractère dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="e114f-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="e114f-115">Pour toutes les autres clés, la valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e114f-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e114f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e114f-116">Requirements</span></span>



| <span data-ttu-id="e114f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e114f-117">Requirement</span></span> | <span data-ttu-id="e114f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e114f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e114f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e114f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e114f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e114f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e114f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e114f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e114f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e114f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e114f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e114f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e114f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e114f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






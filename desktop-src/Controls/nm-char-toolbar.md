---
title: Code de notification NM_CHAR (barre d’outils) (commctrl. h)
description: Envoyé par une barre d’outils lorsqu’il reçoit un \_ message WM char. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Contrôles Windows de code de notification NM_CHAR (barre d’outils)
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
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844469"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="fcc6e-105">\_Code de notification nm caractère (barre d’outils)</span><span class="sxs-lookup"><span data-stu-id="fcc6e-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="fcc6e-106">Envoyé par une barre d’outils lorsqu’il reçoit un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="fcc6e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fcc6e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcc6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcc6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc6e-110">Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient des informations supplémentaires sur le caractère qui a provoqué le code de notification.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="fcc6e-111">Le membre **dwItemPrev** de cette structure contient l’identificateur de commande de l’élément qui est actuellement chaud ou-1 si aucun élément n’est actuellement chaud.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="fcc6e-112">Le membre **dwItemNext** de cette structure contient l’identificateur de commande de l’élément qui devient actif ou-1 si la clé ne correspond pas à l’accélérateur d’un élément.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc6e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcc6e-113">Return value</span></span>

<span data-ttu-id="fcc6e-114">Retourne la **valeur true** pour indiquer que la barre d’outils ne doit pas traiter le caractère et **false** pour que la barre d’outils traite le caractère.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc6e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcc6e-115">Requirements</span></span>



| <span data-ttu-id="fcc6e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcc6e-116">Requirement</span></span> | <span data-ttu-id="fcc6e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcc6e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc6e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcc6e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc6e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcc6e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcc6e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcc6e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc6e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcc6e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcc6e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcc6e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcc6e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc6e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


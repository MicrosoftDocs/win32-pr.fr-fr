---
title: BN_UNPUSHED le code de notification (winuser. h)
description: Envoyé lorsque l’état de transmission d’un bouton a la valeur unpushd.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- Contrôles Windows de code de notification BN_UNPUSHED
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103128"
---
# <a name="bn_unpushed-notification-code"></a><span data-ttu-id="96d73-104">Code de notification de type de transfert de la \_ cale</span><span class="sxs-lookup"><span data-stu-id="96d73-104">BN\_UNPUSHED notification code</span></span>

<span data-ttu-id="96d73-105">Envoyé lorsque l’état de transmission d’un bouton a la valeur unpushd.</span><span class="sxs-lookup"><span data-stu-id="96d73-105">Sent when the push state of a button is set to unpushed.</span></span>

> [!Note]  
> <span data-ttu-id="96d73-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="96d73-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="96d73-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="96d73-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="96d73-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="96d73-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="96d73-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96d73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d73-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96d73-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96d73-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="96d73-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="96d73-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="96d73-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="96d73-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96d73-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96d73-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="96d73-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96d73-115">Notes</span><span class="sxs-lookup"><span data-stu-id="96d73-115">Remarks</span></span>

<span data-ttu-id="96d73-116">\_La fonction de Push n’a pas été envoyée est la même que le code de notification [ \_ UNHILITE](bn-unhilite.md) .</span><span class="sxs-lookup"><span data-stu-id="96d73-116">BN\_UNPUSHED is the same as the [BN\_UNHILITE](bn-unhilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d73-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96d73-117">Requirements</span></span>



| <span data-ttu-id="96d73-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96d73-118">Requirement</span></span> | <span data-ttu-id="96d73-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="96d73-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d73-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96d73-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96d73-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96d73-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96d73-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96d73-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96d73-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96d73-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96d73-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="96d73-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d73-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96d73-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96d73-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96d73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d73-127">pas de \_ pousse</span><span class="sxs-lookup"><span data-stu-id="96d73-127">BN\_PUSHED</span></span>](bn-pushed.md)
</dt> </dl>

 


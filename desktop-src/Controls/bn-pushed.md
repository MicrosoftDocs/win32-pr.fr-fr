---
title: BN_PUSHED le code de notification (winuser. h)
description: Envoyé lorsque l’état de transmission d’un bouton est défini sur Push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- Contrôles Windows de code de notification BN_PUSHED
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317178"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="8c02a-104">\_Code de notification push de la pousse</span><span class="sxs-lookup"><span data-stu-id="8c02a-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="8c02a-105">Envoyé lorsque l’état de transmission d’un bouton est défini sur Push.</span><span class="sxs-lookup"><span data-stu-id="8c02a-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="8c02a-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="8c02a-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="8c02a-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="8c02a-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="8c02a-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8c02a-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8c02a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c02a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c02a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c02a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c02a-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="8c02a-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="8c02a-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="8c02a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8c02a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c02a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c02a-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="8c02a-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c02a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8c02a-115">Remarks</span></span>

<span data-ttu-id="8c02a-116">L’envoi d' \_ un push est le même que le code de notification [ \_ HiLite](bn-hilite.md) .</span><span class="sxs-lookup"><span data-stu-id="8c02a-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c02a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c02a-117">Requirements</span></span>



| <span data-ttu-id="8c02a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c02a-118">Requirement</span></span> | <span data-ttu-id="8c02a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c02a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c02a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c02a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c02a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c02a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c02a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c02a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c02a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c02a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c02a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c02a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c02a-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c02a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c02a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c02a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c02a-127">**aucune \_ transmission de type push**</span><span class="sxs-lookup"><span data-stu-id="8c02a-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 


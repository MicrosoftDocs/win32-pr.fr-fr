---
title: BN_DBLCLK le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur double-clique sur un bouton.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Contrôles Windows de code de notification BN_DBLCLK
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032625"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="dedd0-104">\_Code de notification DBLCLKy</span><span class="sxs-lookup"><span data-stu-id="dedd0-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="dedd0-105">Envoyé lorsque l’utilisateur double-clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="dedd0-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="dedd0-106">Ce code de notification est envoyé automatiquement pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="dedd0-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="dedd0-107">Les autres types de bouton envoient \_ l’DBLCLK de l’adresse de l’utilisateur uniquement s’ils ont le style [**BS \_ Notify**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="dedd0-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="dedd0-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="dedd0-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="dedd0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dedd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedd0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dedd0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dedd0-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="dedd0-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="dedd0-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="dedd0-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="dedd0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dedd0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dedd0-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="dedd0-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dedd0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dedd0-115">Remarks</span></span>

<span data-ttu-id="dedd0-116">L' \_ DBLCLK [de la \_ ](bn-doubleclicked.md) fonction est le même que le code de notification par erreur.</span><span class="sxs-lookup"><span data-stu-id="dedd0-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedd0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dedd0-117">Requirements</span></span>



| <span data-ttu-id="dedd0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dedd0-118">Requirement</span></span> | <span data-ttu-id="dedd0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dedd0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dedd0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd0-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dedd0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dedd0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dedd0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dedd0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dedd0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dedd0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedd0-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dedd0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedd0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dedd0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="dedd0-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dedd0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dedd0-128">sur lequel l' \_ utilisateur a cliqué</span><span class="sxs-lookup"><span data-stu-id="dedd0-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="dedd0-129">Par le biais du double \_</span><span class="sxs-lookup"><span data-stu-id="dedd0-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="dedd0-130">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="dedd0-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dedd0-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="dedd0-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


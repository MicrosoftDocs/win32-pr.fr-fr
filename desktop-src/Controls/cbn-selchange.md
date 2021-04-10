---
title: CBN_SELCHANGE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur modifie la sélection actuelle dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- Contrôles Windows de code de notification CBN_SELCHANGE
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942850"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="a7d03-104">\_Code de notification CBN selChange</span><span class="sxs-lookup"><span data-stu-id="a7d03-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="a7d03-105">Envoyé lorsque l’utilisateur modifie la sélection actuelle dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7d03-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="a7d03-106">L’utilisateur peut modifier la sélection en cliquant dans la zone de liste ou en utilisant les touches de direction.</span><span class="sxs-lookup"><span data-stu-id="a7d03-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="a7d03-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a7d03-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a7d03-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7d03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7d03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d03-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7d03-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="a7d03-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="a7d03-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a7d03-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7d03-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d03-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7d03-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7d03-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a7d03-114">Remarks</span></span>

<span data-ttu-id="a7d03-115">Pour récupérer l’index de la sélection actuelle, envoyez le message [**CB \_ GETCURSEL**](cb-getcursel.md) au contrôle.</span><span class="sxs-lookup"><span data-stu-id="a7d03-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="a7d03-116">Le \_ Code de notification CBN selChange n’est pas envoyé lorsque la sélection actuelle est définie à l’aide du message [**CB \_ SETCURSEL**](cb-setcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d03-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d03-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7d03-117">Requirements</span></span>



| <span data-ttu-id="a7d03-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7d03-118">Requirement</span></span> | <span data-ttu-id="a7d03-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7d03-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d03-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7d03-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d03-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7d03-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7d03-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7d03-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d03-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7d03-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7d03-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7d03-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d03-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d03-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d03-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7d03-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7d03-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a7d03-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7d03-128">CBN \_ gros plan</span><span class="sxs-lookup"><span data-stu-id="a7d03-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="a7d03-129">CBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="a7d03-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="a7d03-130">**\_GETCURSEL CB**</span><span class="sxs-lookup"><span data-stu-id="a7d03-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="a7d03-131">**\_SETCURSEL CB**</span><span class="sxs-lookup"><span data-stu-id="a7d03-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="a7d03-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="a7d03-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a7d03-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7d03-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a7d03-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7d03-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a7d03-135">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="a7d03-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


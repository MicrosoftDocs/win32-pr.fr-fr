---
title: CBN_EDITUPDATE le code de notification (winuser. h)
description: Envoyé lorsque la partie du contrôle d’édition d’une zone de liste déroulante est sur le paragraphe d’afficher du texte modifié.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- Contrôles Windows de code de notification CBN_EDITUPDATE
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106285"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="d76dc-104">\_Code de notification CBN EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="d76dc-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="d76dc-105">Envoyé lorsque la partie du contrôle d’édition d’une zone de liste déroulante est sur le paragraphe d’afficher du texte modifié.</span><span class="sxs-lookup"><span data-stu-id="d76dc-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="d76dc-106">Ce code de notification est envoyé une fois que le contrôle a mis en forme le texte, mais avant d’afficher le texte.</span><span class="sxs-lookup"><span data-stu-id="d76dc-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="d76dc-107">La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d76dc-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d76dc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d76dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d76dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76dc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d76dc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d76dc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d76dc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d76dc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d76dc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76dc-113">Handle vers la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d76dc-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d76dc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d76dc-114">Remarks</span></span>

<span data-ttu-id="d76dc-115">Si la zone de liste déroulante a le style [**\_ DropDownList SCC**](combo-box-styles.md) , ce code de notification n’est pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="d76dc-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76dc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d76dc-116">Requirements</span></span>



| <span data-ttu-id="d76dc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d76dc-117">Requirement</span></span> | <span data-ttu-id="d76dc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d76dc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76dc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d76dc-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76dc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d76dc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d76dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d76dc-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d76dc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d76dc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d76dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76dc-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d76dc-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d76dc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d76dc-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d76dc-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d76dc-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d76dc-127">CBN \_ EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="d76dc-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="d76dc-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d76dc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d76dc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d76dc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d76dc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d76dc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d76dc-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="d76dc-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


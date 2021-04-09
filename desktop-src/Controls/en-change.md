---
title: EN_CHANGE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur a effectué une action qui peut avoir modifié du texte dans un contrôle d’édition.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- Contrôles Windows de code de notification EN_CHANGE
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843357"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="fa08e-104">\_Code de notification de modification</span><span class="sxs-lookup"><span data-stu-id="fa08e-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="fa08e-105">Envoyé lorsque l’utilisateur a effectué une action qui peut avoir modifié du texte dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa08e-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="fa08e-106">Contrairement au code de notification en [ \_ mise à jour](en-update.md) , ce code de notification est envoyé une fois que le système a mis à jour l’écran.</span><span class="sxs-lookup"><span data-stu-id="fa08e-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="fa08e-107">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="fa08e-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="fa08e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa08e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa08e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa08e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa08e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa08e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="fa08e-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="fa08e-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fa08e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa08e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa08e-113">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="fa08e-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa08e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fa08e-114">Remarks</span></span>

<span data-ttu-id="fa08e-115">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fa08e-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fa08e-116">Pour recevoir les \_ codes de notification de modification, spécifiez [**ENM \_ change**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="fa08e-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="fa08e-117">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="fa08e-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="fa08e-118">Le \_ Code de notification de modification n’est pas envoyé lorsque le style de [**\_ multiligne es**](edit-control-styles.md) est utilisé et que le texte est envoyé par le biais de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="fa08e-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa08e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa08e-119">Requirements</span></span>



| <span data-ttu-id="fa08e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa08e-120">Requirement</span></span> | <span data-ttu-id="fa08e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa08e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa08e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa08e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa08e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa08e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa08e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa08e-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa08e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa08e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa08e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa08e-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa08e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa08e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa08e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa08e-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fa08e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa08e-130">en cours de \_ mise à jour</span><span class="sxs-lookup"><span data-stu-id="fa08e-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="fa08e-131">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="fa08e-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fa08e-132">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="fa08e-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


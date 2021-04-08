---
title: Code de notification EN_OLEOPFAILED (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’une action de l’utilisateur sur un objet COM (Component Object Model) a échoué. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- Contrôles Windows de code de notification EN_OLEOPFAILED
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843673"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="88a1e-105">\_Code de notification en OLEOPFAILED</span><span class="sxs-lookup"><span data-stu-id="88a1e-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="88a1e-106">Avertit une fenêtre parente d’un contrôle RichEdit qu’une action de l’utilisateur sur un objet COM (Component Object Model) a échoué.</span><span class="sxs-lookup"><span data-stu-id="88a1e-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="88a1e-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="88a1e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="88a1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88a1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88a1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88a1e-110">Structure [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) qui contient des informations sur l’échec.</span><span class="sxs-lookup"><span data-stu-id="88a1e-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a1e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88a1e-111">Return value</span></span>

<span data-ttu-id="88a1e-112">Ce code de notification retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="88a1e-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a1e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="88a1e-113">Remarks</span></span>

<span data-ttu-id="88a1e-114">La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="88a1e-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88a1e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88a1e-115">Requirements</span></span>



| <span data-ttu-id="88a1e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88a1e-116">Requirement</span></span> | <span data-ttu-id="88a1e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="88a1e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88a1e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88a1e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="88a1e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88a1e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88a1e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88a1e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="88a1e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88a1e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88a1e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="88a1e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="88a1e-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="88a1e-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88a1e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88a1e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="88a1e-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="88a1e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88a1e-126">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="88a1e-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 






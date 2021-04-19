---
description: Une application envoie le \_ message WM MDIREFRESHMENU à une fenêtre cliente d’interface multidocument (MDI) pour actualiser le menu fenêtre de la fenêtre frame MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Message WM_MDIREFRESHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527483"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="17546-103">\_Message WM MDIREFRESHMENU</span><span class="sxs-lookup"><span data-stu-id="17546-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="17546-104">Une application envoie le message **WM \_ MDIREFRESHMENU** à une fenêtre cliente d’interface multidocument (MDI) pour actualiser le menu fenêtre de la fenêtre frame MDI.</span><span class="sxs-lookup"><span data-stu-id="17546-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="17546-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17546-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17546-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17546-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17546-107">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="17546-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="17546-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17546-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17546-109">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="17546-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17546-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17546-110">Return value</span></span>

<span data-ttu-id="17546-111">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="17546-111">Type: **HMENU**</span></span>

<span data-ttu-id="17546-112">Si le message est correctement exécuté, la valeur de retour est le handle du menu de la fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="17546-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="17546-113">Si le message échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="17546-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17546-114">Notes</span><span class="sxs-lookup"><span data-stu-id="17546-114">Remarks</span></span>

<span data-ttu-id="17546-115">Après l’envoi de ce message, une application doit appeler la fonction [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) pour mettre à jour la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="17546-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="17546-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17546-116">Requirements</span></span>



| <span data-ttu-id="17546-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17546-117">Requirement</span></span> | <span data-ttu-id="17546-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="17546-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17546-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17546-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17546-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17546-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17546-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17546-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17546-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17546-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17546-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="17546-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17546-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17546-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17546-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17546-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="17546-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="17546-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17546-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="17546-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="17546-128">**\_MDISETMENU WM**</span><span class="sxs-lookup"><span data-stu-id="17546-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="17546-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="17546-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17546-130">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="17546-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 

---
description: Une application envoie le \_ message WM MDISETMENU à une fenêtre cliente d’interface multidocument (MDI) pour remplacer le menu entier d’une fenêtre frame MDI, pour remplacer le menu fenêtre de la fenêtre frame, ou les deux.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Message WM_MDISETMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527482"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="a2eb3-103">\_Message WM MDISETMENU</span><span class="sxs-lookup"><span data-stu-id="a2eb3-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="a2eb3-104">Une application envoie le message **WM \_ MDISETMENU** à une fenêtre cliente d’interface multidocument (MDI) pour remplacer le menu entier d’une fenêtre frame MDI, pour remplacer le menu fenêtre de la fenêtre frame, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="a2eb3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2eb3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2eb3-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2eb3-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2eb3-107">Handle vers le menu de la nouvelle fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="a2eb3-108">Si ce paramètre a la **valeur null**, le menu de la fenêtre frame n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="a2eb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2eb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2eb3-110">Handle vers le nouveau menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-110">A handle to the new window menu.</span></span> <span data-ttu-id="a2eb3-111">Si ce paramètre a la **valeur null**, le menu fenêtre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2eb3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2eb3-112">Return value</span></span>

<span data-ttu-id="a2eb3-113">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-113">Type: **HMENU**</span></span>

<span data-ttu-id="a2eb3-114">Si le message est correctement exécuté, la valeur de retour est le handle du menu de la fenêtre frame précédente.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="a2eb3-115">Si le message échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2eb3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a2eb3-116">Remarks</span></span>

<span data-ttu-id="a2eb3-117">Après l’envoi de ce message, une application doit appeler la fonction [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) pour mettre à jour la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="a2eb3-118">Si ce message remplace le menu fenêtre, les éléments de menu de la fenêtre enfant MDI sont supprimés du menu fenêtre précédente et ajoutés au menu nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="a2eb3-119">Si une fenêtre enfant MDI est agrandie et que ce message remplace le menu fenêtre frame MDI, l’icône de menu fenêtre et l’icône de restauration sont supprimées du menu de la fenêtre frame précédente et ajoutées au menu nouvelle fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="a2eb3-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2eb3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2eb3-120">Requirements</span></span>



| <span data-ttu-id="a2eb3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2eb3-121">Requirement</span></span> | <span data-ttu-id="a2eb3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2eb3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eb3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2eb3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2eb3-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2eb3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2eb3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2eb3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2eb3-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2eb3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2eb3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2eb3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2eb3-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2eb3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2eb3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2eb3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2eb3-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a2eb3-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="a2eb3-132">**\_MDIREFRESHMENU WM**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="a2eb3-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a2eb3-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a2eb3-134">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="a2eb3-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 

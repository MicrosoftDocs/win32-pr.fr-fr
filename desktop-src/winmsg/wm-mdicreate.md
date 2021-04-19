---
description: Une application envoie le \_ message WM MDICREATE à une fenêtre cliente d’interface multidocument (MDI) pour créer une fenêtre enfant MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Message WM_MDICREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524326"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="35030-103">\_Message WM MDICREATE</span><span class="sxs-lookup"><span data-stu-id="35030-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="35030-104">Une application envoie le message **WM \_ MDICREATE** à une fenêtre cliente d’interface multidocument (MDI) pour créer une fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="35030-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="35030-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35030-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35030-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35030-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35030-107">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="35030-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35030-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35030-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35030-109">Pointeur vers une structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) contenant des informations que le système utilise pour créer la fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="35030-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35030-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35030-110">Return value</span></span>

<span data-ttu-id="35030-111">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="35030-111">Type: **HWND**</span></span>

<span data-ttu-id="35030-112">Si le message est correctement exécuté, la valeur de retour est le handle de la nouvelle fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="35030-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="35030-113">Si le message échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="35030-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35030-114">Notes</span><span class="sxs-lookup"><span data-stu-id="35030-114">Remarks</span></span>

<span data-ttu-id="35030-115">La fenêtre enfant MDI est créée avec le [**style de fenêtre**](window-styles.md) bits **WS \_ Child**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** et **WS \_ MAXIMIZEBOX**, ainsi que les bits de style supplémentaires spécifiés dans la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="35030-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="35030-116">Le système ajoute le titre de la nouvelle fenêtre enfant au menu fenêtre de la fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="35030-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="35030-117">Une application doit utiliser ce message pour créer toutes les fenêtres enfants de la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="35030-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="35030-118">Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.</span><span class="sxs-lookup"><span data-stu-id="35030-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="35030-119">Quand une fenêtre enfant MDI est créée, le système envoie le message [**WM \_ Create**](wm-create.md) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="35030-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="35030-120">Le paramètre *lParam* du message **WM \_ Create** contient un pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="35030-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="35030-121">Le membre *lpCreateParams* de cette structure contient un pointeur vers la structure [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passée avec le message **WM \_ MDICREATE** qui a créé la fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="35030-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="35030-122">Une application ne doit pas envoyer un deuxième message **WM \_ MDICREATE** lorsqu’un message **WM \_ MDICREATE** est toujours en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="35030-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="35030-123">Par exemple, il ne doit pas envoyer de message **WM \_ MDICREATE** lorsqu’une fenêtre enfant MDI traite son message **WM \_ MDICREATE** .</span><span class="sxs-lookup"><span data-stu-id="35030-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="35030-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35030-124">Requirements</span></span>



| <span data-ttu-id="35030-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35030-125">Requirement</span></span> | <span data-ttu-id="35030-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="35030-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35030-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35030-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35030-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35030-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35030-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35030-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35030-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35030-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35030-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="35030-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35030-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35030-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35030-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35030-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="35030-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="35030-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35030-135">**CreateMDIWindow**</span><span class="sxs-lookup"><span data-stu-id="35030-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="35030-136">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="35030-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="35030-137">**MDICREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="35030-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="35030-138">**création de WM \_**</span><span class="sxs-lookup"><span data-stu-id="35030-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="35030-139">**\_MDIDESTROY WM**</span><span class="sxs-lookup"><span data-stu-id="35030-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="35030-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="35030-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35030-141">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="35030-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 

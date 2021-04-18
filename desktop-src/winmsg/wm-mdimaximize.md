---
description: Une application envoie le \_ message WM MDIMAXIMIZE à une fenêtre cliente d’interface multidocument (MDI) pour agrandir une fenêtre enfant MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Message WM_MDIMAXIMIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515996"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="0f6bf-103">\_Message WM MDIMAXIMIZE</span><span class="sxs-lookup"><span data-stu-id="0f6bf-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="0f6bf-104">Une application envoie le message **WM \_ MDIMAXIMIZE** à une fenêtre cliente d’interface multidocument (MDI) pour agrandir une fenêtre enfant MDI.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="0f6bf-105">Le système redimensionne la fenêtre enfant pour que sa zone cliente remplisse la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="0f6bf-106">Le système place l’icône de menu fenêtre de la fenêtre enfant à la position la plus à droite de la barre de menus de la fenêtre frame et place l’icône de restauration de la fenêtre enfant à la position la plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="0f6bf-107">Le système ajoute également le texte de la barre de titre de la fenêtre enfant à celle de la fenêtre frame.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="0f6bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f6bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f6bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6bf-110">Handle vers la fenêtre enfant MDI à agrandir.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="0f6bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f6bf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6bf-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6bf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f6bf-113">Return value</span></span>

<span data-ttu-id="0f6bf-114">Type : **zéro**</span><span class="sxs-lookup"><span data-stu-id="0f6bf-114">Type: **zero**</span></span>

<span data-ttu-id="0f6bf-115">La valeur de retour est toujours zéro.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6bf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0f6bf-116">Remarks</span></span>

<span data-ttu-id="0f6bf-117">Si une fenêtre cliente MDI reçoit un message qui modifie l’activation de ses fenêtres enfants alors que la fenêtre enfant MDI active est agrandie, le système restaure la fenêtre enfant active et agrandit la fenêtre enfant qui vient d’être activée.</span><span class="sxs-lookup"><span data-stu-id="0f6bf-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6bf-118">Requirements</span></span>



| <span data-ttu-id="0f6bf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f6bf-119">Requirement</span></span> | <span data-ttu-id="0f6bf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f6bf-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6bf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6bf-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6bf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0f6bf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6bf-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6bf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f6bf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f6bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6bf-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f6bf-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6bf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6bf-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f6bf-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0f6bf-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f6bf-129">**\_MDIRESTORE WM**</span><span class="sxs-lookup"><span data-stu-id="0f6bf-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="0f6bf-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0f6bf-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f6bf-131">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="0f6bf-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





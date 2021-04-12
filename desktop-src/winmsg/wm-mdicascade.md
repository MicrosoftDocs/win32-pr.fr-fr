---
description: Une application envoie le \_ message WM MDICASCADE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants dans un format en cascade.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Message WM_MDICASCADE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318257"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="e6de1-103">\_Message WM MDICASCADE</span><span class="sxs-lookup"><span data-stu-id="e6de1-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="e6de1-104">Une application envoie le message **WM \_ MDICASCADE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants dans un format en cascade.</span><span class="sxs-lookup"><span data-stu-id="e6de1-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="e6de1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6de1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6de1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6de1-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6de1-107">Comportement en cascade.</span><span class="sxs-lookup"><span data-stu-id="e6de1-107">The cascade behavior.</span></span> <span data-ttu-id="e6de1-108">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6de1-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e6de1-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6de1-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="e6de1-110">Signification</span><span class="sxs-lookup"><span data-stu-id="e6de1-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="e6de1-111"><dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e6de1-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="e6de1-112">Empêche la mise en cascade des fenêtres enfants MDI désactivées.</span><span class="sxs-lookup"><span data-stu-id="e6de1-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="e6de1-113"><dt>**MDITILE \_ ZORDER**</dt> , <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e6de1-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="e6de1-114">Réorganise les fenêtres dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="e6de1-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="e6de1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6de1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6de1-116">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e6de1-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6de1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6de1-117">Return value</span></span>

<span data-ttu-id="e6de1-118">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="e6de1-118">Type: **BOOL**</span></span>

<span data-ttu-id="e6de1-119">Si le message est correctement exécuté, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="e6de1-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="e6de1-120">Si le message échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="e6de1-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6de1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6de1-121">Requirements</span></span>



| <span data-ttu-id="e6de1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6de1-122">Requirement</span></span> | <span data-ttu-id="e6de1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6de1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6de1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6de1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6de1-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6de1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6de1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6de1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6de1-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6de1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6de1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6de1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6de1-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6de1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6de1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6de1-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6de1-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e6de1-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6de1-132">**\_MDIICONARRANGE WM**</span><span class="sxs-lookup"><span data-stu-id="e6de1-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="e6de1-133">**\_MDITILE WM**</span><span class="sxs-lookup"><span data-stu-id="e6de1-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="e6de1-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e6de1-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6de1-135">Interface multidocument</span><span class="sxs-lookup"><span data-stu-id="e6de1-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





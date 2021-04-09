---
description: Envoyé à une icône lorsque l’utilisateur demande que la fenêtre soit restaurée à sa taille et à sa position précédentes.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Message WM_QUERYOPEN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034531"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="d1dfe-103">\_Message WM QUERYOPEN</span><span class="sxs-lookup"><span data-stu-id="d1dfe-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="d1dfe-104">Envoyé à une icône lorsque l’utilisateur demande que la fenêtre soit restaurée à sa taille et à sa position précédentes.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="d1dfe-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1dfe-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="d1dfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1dfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1dfe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1dfe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1dfe-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1dfe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1dfe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1dfe-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1dfe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1dfe-111">Return value</span></span>

<span data-ttu-id="d1dfe-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1dfe-112">Type: **LRESULT**</span></span>

<span data-ttu-id="d1dfe-113">Si l’icône peut être ouverte, une application qui traite ce message doit retourner la **valeur true**; Sinon, elle doit retourner **false** pour empêcher l’ouverture de l’icône.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1dfe-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d1dfe-114">Remarks</span></span>

<span data-ttu-id="d1dfe-115">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d1dfe-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="d1dfe-116">Lors du traitement de ce message, l’application ne doit effectuer aucune action qui entraînerait une modification de l’activation ou du focus (par exemple, la création d’une boîte de dialogue).</span><span class="sxs-lookup"><span data-stu-id="d1dfe-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1dfe-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1dfe-117">Requirements</span></span>



| <span data-ttu-id="d1dfe-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1dfe-118">Requirement</span></span> | <span data-ttu-id="d1dfe-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1dfe-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dfe-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1dfe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1dfe-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1dfe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1dfe-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1dfe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1dfe-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1dfe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1dfe-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1dfe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1dfe-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfe-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1dfe-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1dfe-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1dfe-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d1dfe-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1dfe-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d1dfe-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="d1dfe-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d1dfe-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1dfe-130">Windows</span><span class="sxs-lookup"><span data-stu-id="d1dfe-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 

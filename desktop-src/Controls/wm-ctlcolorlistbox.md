---
title: Message WM_CTLCOLORLISTBOX (winuser. h)
description: Envoyé à la fenêtre parente d’une zone de liste avant que le système ne dessine la zone de liste. En répondant à ce message, la fenêtre parente peut définir les couleurs de texte et d’arrière-plan de la zone de liste à l’aide du handle de contexte de périphérique d’affichage spécifié.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103548"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="26b74-105">\_Message WM CTLCOLORLISTBOX</span><span class="sxs-lookup"><span data-stu-id="26b74-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="26b74-106">Envoyé à la fenêtre parente d’une zone de liste avant que le système ne dessine la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="26b74-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="26b74-107">En répondant à ce message, la fenêtre parente peut définir les couleurs de texte et d’arrière-plan de la zone de liste à l’aide du handle de contexte de périphérique d’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="26b74-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="26b74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26b74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26b74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26b74-110">Handle vers le contexte de périphérique pour la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="26b74-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="26b74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26b74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26b74-112">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="26b74-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b74-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26b74-113">Return value</span></span>

<span data-ttu-id="26b74-114">Si une application traite ce message, elle doit retourner un handle à un pinceau.</span><span class="sxs-lookup"><span data-stu-id="26b74-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="26b74-115">Le système utilise le pinceau pour peindre l’arrière-plan de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="26b74-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b74-116">Notes</span><span class="sxs-lookup"><span data-stu-id="26b74-116">Remarks</span></span>

<span data-ttu-id="26b74-117">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="26b74-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="26b74-118">Le message **WM \_ CTLCOLORLISTBOX** n’est jamais envoyé entre les threads.</span><span class="sxs-lookup"><span data-stu-id="26b74-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="26b74-119">Elle est envoyée uniquement au sein d’un thread.</span><span class="sxs-lookup"><span data-stu-id="26b74-119">It is sent only within one thread.</span></span>

<span data-ttu-id="26b74-120">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="26b74-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="26b74-121">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="26b74-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="26b74-122">La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="26b74-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b74-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26b74-123">Requirements</span></span>



| <span data-ttu-id="26b74-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26b74-124">Requirement</span></span> | <span data-ttu-id="26b74-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="26b74-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b74-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26b74-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26b74-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26b74-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26b74-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26b74-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26b74-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26b74-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26b74-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="26b74-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b74-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26b74-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b74-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26b74-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="26b74-133">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="26b74-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="26b74-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="26b74-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="26b74-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="26b74-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="26b74-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="26b74-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 


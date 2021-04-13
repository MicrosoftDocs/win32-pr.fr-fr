---
title: Message WM_RENDERALLFORMATS (winuser. h)
description: Envoyé au propriétaire du presse-papiers avant sa destruction, si le propriétaire du presse-papiers a retardé le rendu d’un ou de plusieurs formats de presse-papiers.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS l’échange de données de message
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509093"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="4d376-104">\_Message WM RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="4d376-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="4d376-105">Envoyé au propriétaire du presse-papiers avant sa destruction, si le propriétaire du presse-papiers a retardé le rendu d’un ou de plusieurs formats de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4d376-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="4d376-106">Pour que le contenu du presse-papiers reste disponible pour d’autres applications, le propriétaire du presse-papiers doit restituer les données dans tous les formats qu’il est en charge de générer et placer les données dans le presse-papiers en appelant la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="4d376-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="4d376-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4d376-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="4d376-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d376-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d376-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d376-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d376-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4d376-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d376-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d376-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d376-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4d376-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d376-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d376-113">Return value</span></span>

<span data-ttu-id="4d376-114">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="4d376-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d376-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4d376-115">Remarks</span></span>

<span data-ttu-id="4d376-116">Lors de la réponse à un message **WM \_ RENDERALLFORMATS** , l’application doit appeler la fonction [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) , puis vérifier qu’elle est toujours le propriétaire du presse-papiers en appelant la fonction [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="4d376-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="4d376-117">L’application doit vérifier qu’elle est toujours le propriétaire du presse-papiers après avoir ouvert le presse-papiers, car après avoir reçu le message **WM \_ RENDERALLFORMATS** , mais avant d’ouvrir le presse-papiers, une autre application a peut-être ouvert et pris possession du presse-papiers, et les données de cette application ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="4d376-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="4d376-118">Dans la plupart des cas, l’application ne doit pas appeler la fonction [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), car cela entraînera l’effacement des formats de presse-papiers que l’application a déjà rendus.</span><span class="sxs-lookup"><span data-stu-id="4d376-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="4d376-119">Lorsque l’application est retournée, le système supprime tous les formats non rendus de la liste des formats de presse-papiers disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d376-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="4d376-120">Pour plus d’informations sur le rendu retardé, consultez [rendu retardé](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="4d376-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d376-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d376-121">Requirements</span></span>



| <span data-ttu-id="4d376-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d376-122">Requirement</span></span> | <span data-ttu-id="4d376-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d376-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d376-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d376-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d376-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d376-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4d376-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d376-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d376-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d376-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d376-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d376-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d376-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d376-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d376-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d376-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d376-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4d376-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d376-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="4d376-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="4d376-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="4d376-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="4d376-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="4d376-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="4d376-135">**\_RENDERFORMAT WM**</span><span class="sxs-lookup"><span data-stu-id="4d376-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="4d376-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4d376-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d376-137">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="4d376-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


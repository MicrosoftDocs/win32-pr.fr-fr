---
title: Message WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indique à une fenêtre de fournir une image bitmap statique à utiliser comme aperçu instantané (également appelé aperçu de lecture) de cette fenêtre.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Message de WM_DWMSENDICONICLIVEPREVIEWBITMAP Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465498"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="71902-104">\_Message WM DWMSENDICONICLIVEPREVIEWBITMAP</span><span class="sxs-lookup"><span data-stu-id="71902-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="71902-105">Indique à une fenêtre de fournir une image bitmap statique à utiliser comme *aperçu instantané* (également appelé aperçu de *lecture*) de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="71902-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71902-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71902-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71902-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="71902-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="71902-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71902-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71902-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="71902-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71902-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71902-111">Return value</span></span>

<span data-ttu-id="71902-112">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="71902-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="71902-113">Notes</span><span class="sxs-lookup"><span data-stu-id="71902-113">Remarks</span></span>

<span data-ttu-id="71902-114">Un *aperçu instantané* (également appelé *Aperçu avant impression*) d’une fenêtre s’affiche lorsqu’un utilisateur déplace le pointeur de la souris sur la miniature de la fenêtre dans la barre des tâches ou donne le focus de la miniature dans la fenêtre ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="71902-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="71902-115">Cette vue est un aperçu complet de la fenêtre et peut être un instantané en direct ou une représentation sous forme.</span><span class="sxs-lookup"><span data-stu-id="71902-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="71902-116">Gestionnaire de fenêtrage (DWM) envoie ce message à une fenêtre si toutes les situations suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="71902-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="71902-117">L’aperçu instantané a été appelé dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="71902-118">[**DWMWA a l’attribut \_ \_ \_ bitmap sous forme**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) est défini dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="71902-119">Une représentation sous forme est la seule qui existe pour cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="71902-120">La fenêtre qui reçoit ce message doit répondre en générant une image bitmap à l’échelle complète.</span><span class="sxs-lookup"><span data-stu-id="71902-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="71902-121">La fenêtre appelle ensuite la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) pour définir l’aperçu instantané.</span><span class="sxs-lookup"><span data-stu-id="71902-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="71902-122">Si la fenêtre ne définit pas de bitmap dans un laps de temps donné, DWM utilise sa propre représentation sous forme par défaut pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="71902-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="71902-123">Examples</span></span>

<span data-ttu-id="71902-124">L’exemple suivant illustre une réponse au message **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** .</span><span class="sxs-lookup"><span data-stu-id="71902-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="71902-125">L’exemple appelle la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) avec un handle vers une image bitmap personnalisée indépendante du périphérique à utiliser comme représentation de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71902-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="71902-126">Pour obtenir le code complet, consultez les exemples de [miniatures Customize a sous forme et Live Preview](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="71902-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="71902-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71902-127">Requirements</span></span>



| <span data-ttu-id="71902-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71902-128">Requirement</span></span> | <span data-ttu-id="71902-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="71902-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71902-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71902-130">Minimum supported client</span></span><br/> | <span data-ttu-id="71902-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71902-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="71902-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71902-132">Minimum supported server</span></span><br/> | <span data-ttu-id="71902-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71902-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71902-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="71902-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="71902-135"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71902-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71902-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71902-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71902-137">**\_DWMSENDICONICTHUMBNAIL WM**</span><span class="sxs-lookup"><span data-stu-id="71902-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="71902-138">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="71902-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 






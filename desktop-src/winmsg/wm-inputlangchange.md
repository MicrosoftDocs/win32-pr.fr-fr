---
description: Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction DefWindowProc, qui le transmet à toutes les fenêtres enfants de premier niveau.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Message WM_INPUTLANGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332404"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="ad5d5-104">\_Message WM INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="ad5d5-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="ad5d5-105">Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="ad5d5-106">Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui le transmet à toutes les fenêtres enfants de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="ad5d5-107">Ces fenêtres enfants peuvent transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour qu’il transmette le message à leurs fenêtres enfants, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="ad5d5-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad5d5-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="ad5d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad5d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5d5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad5d5-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="ad5d5-111">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-111">Type: **WPARAM**</span></span>

<span data-ttu-id="ad5d5-112">[Page de codes](../Intl/code-pages.md) des nouveaux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="ad5d5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad5d5-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="ad5d5-114">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-114">Type: **LPARAM**</span></span>

<span data-ttu-id="ad5d5-115">Identificateur de paramètres régionaux d’entrée **HKL** .</span><span class="sxs-lookup"><span data-stu-id="ad5d5-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="ad5d5-116">Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="ad5d5-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad5d5-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad5d5-117">Return value</span></span>

<span data-ttu-id="ad5d5-118">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-118">Type: **LRESULT**</span></span>

<span data-ttu-id="ad5d5-119">Une application doit retourner une valeur différente de zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5d5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad5d5-120">Remarks</span></span>

<span data-ttu-id="ad5d5-121">Vous pouvez récupérer le [nom des paramètres régionaux](../Intl/locale-names.md) du clavier via la fonction [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) .</span><span class="sxs-lookup"><span data-stu-id="ad5d5-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="ad5d5-122">Avec le nom des paramètres régionaux, vous pouvez utiliser les [fonctions de paramètres régionaux modernes](/windows/win32/intl/calling-the--locale-name--functions):</span><span class="sxs-lookup"><span data-stu-id="ad5d5-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="ad5d5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad5d5-123">Requirements</span></span>

| <span data-ttu-id="ad5d5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad5d5-124">Requirement</span></span> | <span data-ttu-id="ad5d5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad5d5-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5d5-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad5d5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5d5-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad5d5-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad5d5-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad5d5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5d5-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad5d5-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad5d5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad5d5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad5d5-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad5d5-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ad5d5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad5d5-132">See also</span></span>

<span data-ttu-id="ad5d5-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-133">**Reference**</span></span>

- [<span data-ttu-id="ad5d5-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="ad5d5-135">**\_INPUTLANGCHANGEREQUEST WM**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="ad5d5-136">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="ad5d5-136">**Conceptual**</span></span>

- [<span data-ttu-id="ad5d5-137">Windows</span><span class="sxs-lookup"><span data-stu-id="ad5d5-137">Windows</span></span>](windows.md) 

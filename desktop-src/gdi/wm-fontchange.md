---
description: Une application envoie le \_ message WM FONTCHANGE à toutes les fenêtres de niveau supérieur dans le système après la modification du pool de ressources de police.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Message WM_FONTCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973515"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="8f55b-103">\_Message WM FONTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8f55b-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="8f55b-104">Une application envoie le message **WM \_ FONTCHANGE** à toutes les fenêtres de niveau supérieur dans le système après la modification du pool de ressources de police.</span><span class="sxs-lookup"><span data-stu-id="8f55b-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="8f55b-105">Pour envoyer ce message, appelez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="8f55b-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="8f55b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f55b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f55b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f55b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f55b-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8f55b-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f55b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f55b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f55b-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8f55b-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f55b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8f55b-111">Remarks</span></span>

<span data-ttu-id="8f55b-112">Une application qui ajoute ou supprime des polices du système (par exemple, à l’aide de la fonction [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ) doit envoyer ce message à toutes les fenêtres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8f55b-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="8f55b-113">Pour envoyer le message **WM \_ FONTCHANGE** à toutes les fenêtres de niveau supérieur, une application peut appeler la fonction **SendMessage** avec le paramètre *HWND* défini sur \_ Broadcast HWND.</span><span class="sxs-lookup"><span data-stu-id="8f55b-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f55b-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8f55b-114">Requirements</span></span>



| <span data-ttu-id="8f55b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f55b-115">Requirement</span></span> | <span data-ttu-id="8f55b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f55b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f55b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f55b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f55b-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f55b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8f55b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f55b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f55b-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f55b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f55b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f55b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f55b-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f55b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f55b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f55b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f55b-124">Vue d’ensemble des polices et du texte</span><span class="sxs-lookup"><span data-stu-id="8f55b-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="8f55b-125">Polices et messages texte</span><span class="sxs-lookup"><span data-stu-id="8f55b-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="8f55b-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="8f55b-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="8f55b-127">**RemoveFontResource**</span><span class="sxs-lookup"><span data-stu-id="8f55b-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 

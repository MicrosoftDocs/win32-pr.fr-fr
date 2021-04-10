---
title: Message MCIWNDM_REALIZE (VFW. h)
description: Le \_ message MCIWNDM de réalisation réalise la palette actuellement utilisée par le périphérique MCI dans une fenêtre MCIWnd. Cette macro est définie avec le \_ message MCIWNDM. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Message MCIWNDM_REALIZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941733"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="7cb52-106">MCIWNDM \_ réaliser le message</span><span class="sxs-lookup"><span data-stu-id="7cb52-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="7cb52-107">Le **message \_ MCIWNDM** de réalisation réalise la palette actuellement utilisée par le périphérique MCI dans une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="7cb52-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="7cb52-108">Cette macro est définie avec le **message \_ MCIWNDM** .</span><span class="sxs-lookup"><span data-stu-id="7cb52-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="7cb52-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="7cb52-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7cb52-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cb52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb52-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span><span class="sxs-lookup"><span data-stu-id="7cb52-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="7cb52-112">Indicateur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7cb52-112">Background flag.</span></span> <span data-ttu-id="7cb52-113">Spécifiez **true** pour ce paramètre si la fenêtre est une application en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7cb52-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb52-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7cb52-114">Return Value</span></span>

<span data-ttu-id="7cb52-115">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="7cb52-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb52-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7cb52-116">Remarks</span></span>

<span data-ttu-id="7cb52-117">**MCIWNDM \_ RÉALISEz** l’utilisation de la palette du périphérique MCI et appelle la fonction [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) .</span><span class="sxs-lookup"><span data-stu-id="7cb52-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="7cb52-118">Si votre application gère explicitement les messages [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , vous devez utiliser ce message dans votre application au lieu d’utiliser **RealizePalette**.</span><span class="sxs-lookup"><span data-stu-id="7cb52-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="7cb52-119">Si le corps de l’un de ces gestionnaires de messages contient uniquement **RealizePalette**, transférez le message à la fenêtre MCIWnd, qui réalise automatiquement la palette.</span><span class="sxs-lookup"><span data-stu-id="7cb52-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb52-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb52-120">Requirements</span></span>



| <span data-ttu-id="7cb52-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cb52-121">Requirement</span></span> | <span data-ttu-id="7cb52-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb52-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7cb52-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb52-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb52-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb52-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7cb52-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb52-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb52-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb52-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7cb52-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cb52-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb52-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb52-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb52-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cb52-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb52-130">**MCIWndRealize**</span><span class="sxs-lookup"><span data-stu-id="7cb52-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="7cb52-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="7cb52-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="7cb52-132">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="7cb52-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="7cb52-133">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="7cb52-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 


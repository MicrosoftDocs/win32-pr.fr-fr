---
description: Le \_ message WM PALETTEISCHANGING informe les applications qu’une application va réaliser sa palette logique.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Message WM_PALETTEISCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757876"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="d87b6-103">\_Message WM PALETTEISCHANGING</span><span class="sxs-lookup"><span data-stu-id="d87b6-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="d87b6-104">Le message **WM \_ PALETTEISCHANGING** informe les applications qu’une application va réaliser sa palette logique.</span><span class="sxs-lookup"><span data-stu-id="d87b6-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="d87b6-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d87b6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="d87b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d87b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d87b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d87b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d87b6-108">Handle de la fenêtre qui va réaliser sa palette logique.</span><span class="sxs-lookup"><span data-stu-id="d87b6-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="d87b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d87b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d87b6-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d87b6-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d87b6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d87b6-111">Return value</span></span>

<span data-ttu-id="d87b6-112">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d87b6-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d87b6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d87b6-113">Remarks</span></span>

<span data-ttu-id="d87b6-114">L’application qui modifie sa palette n’attend pas d’accusé de réception de ce message avant de modifier la palette et d’envoyer le message [**WM \_ PALETTECHANGED**](wm-palettechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d87b6-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="d87b6-115">Par conséquent, la palette peut déjà être modifiée quand une application reçoit ce message.</span><span class="sxs-lookup"><span data-stu-id="d87b6-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="d87b6-116">Si l’application ignore ou ne parvient pas à traiter ce message et qu’une deuxième application réalise sa palette alors que le premier utilise des index de palette, il est fort probable que l’utilisateur verra des couleurs inattendues pendant les opérations de dessin suivantes.</span><span class="sxs-lookup"><span data-stu-id="d87b6-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87b6-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d87b6-117">Requirements</span></span>



| <span data-ttu-id="d87b6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d87b6-118">Requirement</span></span> | <span data-ttu-id="d87b6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d87b6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d87b6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d87b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d87b6-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d87b6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d87b6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d87b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d87b6-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d87b6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d87b6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d87b6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d87b6-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d87b6-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d87b6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d87b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87b6-127">Vue d’ensemble des couleurs</span><span class="sxs-lookup"><span data-stu-id="d87b6-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="d87b6-128">Messages de couleur</span><span class="sxs-lookup"><span data-stu-id="d87b6-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="d87b6-129">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="d87b6-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="d87b6-130">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="d87b6-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 

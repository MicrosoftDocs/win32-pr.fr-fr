---
title: Message WM_PAINTCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et que la zone cliente de la visionneuse du presse-papiers doit être redessinée.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518074"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="b52ea-104">\_Message WM PAINTCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="b52ea-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="b52ea-105">Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et que la zone cliente de la visionneuse du presse-papiers doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="b52ea-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="b52ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b52ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b52ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b52ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b52ea-108">Handle de la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b52ea-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="b52ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b52ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b52ea-110">Handle d’un objet de mémoire global qui contient une structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="b52ea-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="b52ea-111">La structure définit la partie de la zone cliente à peindre.</span><span class="sxs-lookup"><span data-stu-id="b52ea-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b52ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b52ea-112">Return value</span></span>

<span data-ttu-id="b52ea-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b52ea-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b52ea-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b52ea-114">Remarks</span></span>

<span data-ttu-id="b52ea-115">Pour déterminer si la totalité de la zone cliente ou seulement une partie de celle-ci doit être redessinée, le propriétaire du presse-papiers doit comparer les dimensions de la zone de dessin donnée dans le membre **rcPaint** de [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) aux dimensions indiquées dans le message [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b52ea-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="b52ea-116">Le propriétaire du presse-papiers doit utiliser la fonction [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) pour verrouiller la mémoire qui contient la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="b52ea-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="b52ea-117">Avant de retourner, le propriétaire du presse-papiers doit déverrouiller cette mémoire à l’aide de la fonction [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="b52ea-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52ea-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b52ea-118">Requirements</span></span>



| <span data-ttu-id="b52ea-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b52ea-119">Requirement</span></span> | <span data-ttu-id="b52ea-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b52ea-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52ea-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b52ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b52ea-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b52ea-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b52ea-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b52ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b52ea-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b52ea-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b52ea-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b52ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52ea-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b52ea-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52ea-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b52ea-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b52ea-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b52ea-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b52ea-129">**\_SIZECLIPBOARD WM**</span><span class="sxs-lookup"><span data-stu-id="b52ea-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="b52ea-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b52ea-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b52ea-131">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="b52ea-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


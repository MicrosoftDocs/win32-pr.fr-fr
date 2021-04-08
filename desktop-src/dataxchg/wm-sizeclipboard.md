---
title: Message WM_SIZECLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et que la zone cliente de la visionneuse du presse-papiers a changé de taille.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741861"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="9f572-104">\_Message WM SIZECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="9f572-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="9f572-105">Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et que la zone cliente de la visionneuse du presse-papiers a changé de taille.</span><span class="sxs-lookup"><span data-stu-id="9f572-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="9f572-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f572-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f572-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f572-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f572-108">Handle de la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9f572-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="9f572-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f572-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f572-110">Handle d’un objet de mémoire global qui contient une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f572-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="9f572-111">La structure spécifie les nouvelles dimensions de la zone cliente de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="9f572-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f572-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f572-112">Return value</span></span>

<span data-ttu-id="9f572-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="9f572-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f572-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9f572-114">Remarks</span></span>

<span data-ttu-id="9f572-115">Quand la fenêtre de la visionneuse du presse-papiers est sur le point d’être détruite ou redimensionnée, un message **WM \_ SIZECLIPBOARD** est envoyé avec un rectangle null (0, 0, 0, 0) en tant que nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="9f572-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="9f572-116">Cela permet au propriétaire du presse-papiers de libérer ses ressources d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f572-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="9f572-117">Le propriétaire du presse-papiers doit utiliser la fonction [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) pour verrouiller l’objet mémoire qui contient [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9f572-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="9f572-118">Avant de retourner, le propriétaire du presse-papiers doit déverrouiller l’objet à l’aide de la fonction [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="9f572-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f572-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f572-119">Requirements</span></span>



| <span data-ttu-id="9f572-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f572-120">Requirement</span></span> | <span data-ttu-id="9f572-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f572-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f572-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f572-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f572-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f572-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f572-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f572-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f572-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f572-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f572-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f572-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f572-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f572-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f572-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f572-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f572-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9f572-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f572-130">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="9f572-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


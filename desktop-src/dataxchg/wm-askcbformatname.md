---
title: Message WM_ASKCBFORMATNAME (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers pour demander le nom d’un \_ format de presse-papiers CF OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME l’échange de données de message
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103252"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="babed-104">\_Message WM ASKCBFORMATNAME</span><span class="sxs-lookup"><span data-stu-id="babed-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="babed-105">Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers pour demander le nom d’un format de presse-papiers [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="babed-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="babed-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="babed-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="babed-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="babed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="babed-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="babed-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babed-109">Taille, en caractères, de la mémoire tampon vers laquelle pointe le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="babed-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="babed-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="babed-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babed-111">Pointeur vers la mémoire tampon qui doit recevoir le nom du format du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="babed-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="babed-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="babed-112">Return value</span></span>

<span data-ttu-id="babed-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="babed-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="babed-114">Notes</span><span class="sxs-lookup"><span data-stu-id="babed-114">Remarks</span></span>

<span data-ttu-id="babed-115">En réponse à ce message, le propriétaire du presse-papiers doit copier le nom du format d’affichage du propriétaire dans la mémoire tampon spécifiée, sans dépasser la taille de la mémoire tampon spécifiée par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="babed-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="babed-116">Une fenêtre de la visionneuse du presse-papiers envoie ce message au propriétaire du presse-papiers pour déterminer le nom du format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) , par exemple, pour initialiser un menu répertoriant les formats disponibles.</span><span class="sxs-lookup"><span data-stu-id="babed-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="babed-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="babed-117">Requirements</span></span>



| <span data-ttu-id="babed-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="babed-118">Requirement</span></span> | <span data-ttu-id="babed-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="babed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="babed-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="babed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="babed-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="babed-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="babed-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="babed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="babed-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="babed-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="babed-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="babed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="babed-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="babed-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="babed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="babed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babed-127">Vue d’ensemble du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="babed-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 


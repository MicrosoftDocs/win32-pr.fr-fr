---
title: Message WM_CLIPBOARDUPDATE (winuser. h)
description: Envoyé lorsque le contenu du presse-papiers a changé.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104086"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="15a0d-104">\_Message WM CLIPBOARDUPDATE</span><span class="sxs-lookup"><span data-stu-id="15a0d-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="15a0d-105">Envoyé lorsque le contenu du presse-papiers a changé.</span><span class="sxs-lookup"><span data-stu-id="15a0d-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="15a0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a0d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15a0d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a0d-108">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="15a0d-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="15a0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15a0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a0d-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="15a0d-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a0d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15a0d-111">Return value</span></span>

<span data-ttu-id="15a0d-112">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="15a0d-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a0d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="15a0d-113">Remarks</span></span>

<span data-ttu-id="15a0d-114">Pour inscrire une fenêtre pour recevoir ce message, utilisez la fonction [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="15a0d-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a0d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15a0d-115">Requirements</span></span>



| <span data-ttu-id="15a0d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15a0d-116">Requirement</span></span> | <span data-ttu-id="15a0d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="15a0d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a0d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15a0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15a0d-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15a0d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15a0d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15a0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15a0d-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15a0d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15a0d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="15a0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a0d-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15a0d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a0d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15a0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a0d-125">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="15a0d-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="15a0d-126">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="15a0d-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="15a0d-127">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="15a0d-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 






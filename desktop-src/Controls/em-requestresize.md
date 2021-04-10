---
title: Message EM_REQUESTRESIZE (RichEdit. h)
description: Force un contrôle RichEdit à envoyer un code de \_ notification en REQUESTRESIZE à sa fenêtre parente.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200581"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="9688e-104">\_Message REQUESTRESIZE em</span><span class="sxs-lookup"><span data-stu-id="9688e-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="9688e-105">Force un contrôle RichEdit à envoyer un code de notification en [**\_ REQUESTRESIZE**](en-requestresize.md) à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="9688e-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9688e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9688e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9688e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9688e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9688e-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9688e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9688e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9688e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9688e-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9688e-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9688e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9688e-111">Return value</span></span>

<span data-ttu-id="9688e-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9688e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9688e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9688e-113">Remarks</span></span>

<span data-ttu-id="9688e-114">Ce message est utile lors du traitement de la [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour le parent d’un contrôle Rich Edit sans fin.</span><span class="sxs-lookup"><span data-stu-id="9688e-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9688e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9688e-115">Requirements</span></span>



| <span data-ttu-id="9688e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9688e-116">Requirement</span></span> | <span data-ttu-id="9688e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9688e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9688e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9688e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9688e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9688e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9688e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9688e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9688e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9688e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9688e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9688e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9688e-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9688e-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9688e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9688e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9688e-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9688e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9688e-126">**en \_ REQUESTRESIZE**</span><span class="sxs-lookup"><span data-stu-id="9688e-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="9688e-127">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="9688e-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9688e-128">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="9688e-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 


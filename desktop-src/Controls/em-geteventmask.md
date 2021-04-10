---
title: Message EM_GETEVENTMASK (RichEdit. h)
description: Récupère le masque d’événement pour un contrôle RichEdit. Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942489"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="34c18-105">\_Message GETEVENTMASK em</span><span class="sxs-lookup"><span data-stu-id="34c18-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="34c18-106">Récupère le masque d’événement pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="34c18-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="34c18-107">Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="34c18-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="34c18-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34c18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c18-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34c18-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34c18-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="34c18-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="34c18-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34c18-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34c18-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="34c18-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34c18-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34c18-113">Return value</span></span>

<span data-ttu-id="34c18-114">Ce message retourne le masque d’événement pour le contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="34c18-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="34c18-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34c18-115">Requirements</span></span>



| <span data-ttu-id="34c18-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34c18-116">Requirement</span></span> | <span data-ttu-id="34c18-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="34c18-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34c18-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34c18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34c18-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34c18-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34c18-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34c18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34c18-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34c18-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34c18-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="34c18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="34c18-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c18-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c18-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34c18-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="34c18-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="34c18-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34c18-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="34c18-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="34c18-127">**Indicateurs de masque d’événement de contrôle RichEdit**</span><span class="sxs-lookup"><span data-stu-id="34c18-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 






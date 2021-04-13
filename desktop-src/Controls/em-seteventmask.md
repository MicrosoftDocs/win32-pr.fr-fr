---
title: Message EM_SETEVENTMASK (RichEdit. h)
description: Définit le masque d’événement pour un contrôle RichEdit. Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466542"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="66933-105">\_Message em SETEVENTMASK</span><span class="sxs-lookup"><span data-stu-id="66933-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="66933-106">Définit le masque d’événement pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="66933-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="66933-107">Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="66933-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="66933-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66933-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66933-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66933-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66933-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="66933-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="66933-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66933-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66933-112">Nouveau masque d’événement pour le contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="66933-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="66933-113">Pour obtenir la liste des masques d’événements, consultez [**indicateurs de masque d’événement de contrôle RichEdit**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="66933-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66933-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66933-114">Return value</span></span>

<span data-ttu-id="66933-115">Ce message retourne le masque d’événement précédent.</span><span class="sxs-lookup"><span data-stu-id="66933-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="66933-116">Notes</span><span class="sxs-lookup"><span data-stu-id="66933-116">Remarks</span></span>

<span data-ttu-id="66933-117">Le masque d’événement par défaut (avant tout est défini) est ENM \_ aucun.</span><span class="sxs-lookup"><span data-stu-id="66933-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="66933-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66933-118">Requirements</span></span>



| <span data-ttu-id="66933-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66933-119">Requirement</span></span> | <span data-ttu-id="66933-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="66933-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66933-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66933-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66933-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66933-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66933-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66933-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66933-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66933-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66933-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="66933-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66933-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="66933-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66933-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66933-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="66933-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="66933-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66933-129">**\_GETEVENTMASK em**</span><span class="sxs-lookup"><span data-stu-id="66933-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="66933-130">**Indicateurs de masque d’événement de contrôle RichEdit**</span><span class="sxs-lookup"><span data-stu-id="66933-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 






---
title: Message BCM_SETNOTE (commctrl. h)
description: Définit le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ SetNote macro.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942116"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="05be1-105">\_Message SETNOTE BCM</span><span class="sxs-lookup"><span data-stu-id="05be1-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="05be1-106">Définit le texte de la note associée à un bouton de lien de commande.</span><span class="sxs-lookup"><span data-stu-id="05be1-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="05be1-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span><span class="sxs-lookup"><span data-stu-id="05be1-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="05be1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05be1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05be1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05be1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05be1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="05be1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="05be1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05be1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05be1-112">Pointeur vers une chaîne **WCHAR** se terminant par un caractère null qui contient la note.</span><span class="sxs-lookup"><span data-stu-id="05be1-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05be1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05be1-113">Return value</span></span>

<span data-ttu-id="05be1-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="05be1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="05be1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="05be1-115">Remarks</span></span>

<span data-ttu-id="05be1-116">À partir de la version 6,01 de ComCtl32, les boutons de lien de commande peuvent avoir une note.</span><span class="sxs-lookup"><span data-stu-id="05be1-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="05be1-117">Le **message \_ SETNOTE BCM** fonctionne uniquement avec les styles de bouton [**BS \_ COMMANDLINK**](button-styles.md) et [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="05be1-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="05be1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05be1-118">Requirements</span></span>



| <span data-ttu-id="05be1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05be1-119">Requirement</span></span> | <span data-ttu-id="05be1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05be1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05be1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05be1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05be1-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05be1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05be1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05be1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05be1-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05be1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05be1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="05be1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="05be1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05be1-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05be1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05be1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="05be1-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="05be1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05be1-129">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="05be1-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="05be1-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="05be1-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05be1-131">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="05be1-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 






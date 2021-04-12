---
title: Message BCM_GETNOTELENGTH (commctrl. h)
description: Obtient la longueur du texte de la note qui peut s’afficher dans la description d’un bouton de lien de commande. Envoyez ce message explicitement ou à l’aide de la \_ macro Button GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032763"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="95bd4-105">\_Message GETNOTELENGTH BCM</span><span class="sxs-lookup"><span data-stu-id="95bd4-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="95bd4-106">Obtient la longueur du texte de la note qui peut s’afficher dans la description d’un bouton de lien de commande.</span><span class="sxs-lookup"><span data-stu-id="95bd4-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="95bd4-107">Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) .</span><span class="sxs-lookup"><span data-stu-id="95bd4-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95bd4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95bd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bd4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95bd4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95bd4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95bd4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95bd4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95bd4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95bd4-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95bd4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bd4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95bd4-113">Return value</span></span>

<span data-ttu-id="95bd4-114">Retourne la longueur du texte de la note dans **WCHARs**, à l’exclusion de toute **valeur null** de fin, ou zéro s’il n’y a aucun texte de note.</span><span class="sxs-lookup"><span data-stu-id="95bd4-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bd4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="95bd4-115">Remarks</span></span>

<span data-ttu-id="95bd4-116">À partir de la version 6,01 de ComCtl32, les boutons de lien de commande peuvent avoir une note.</span><span class="sxs-lookup"><span data-stu-id="95bd4-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="95bd4-117">Pour plus d’informations sur les versions de DLL, consultez [versions de contrôle courantes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="95bd4-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="95bd4-118">Le **message \_ GETNOTELENGTH BCM** fonctionne uniquement avec les styles de bouton [**BS \_ COMMANDLINK**](button-styles.md) et [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="95bd4-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bd4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95bd4-119">Requirements</span></span>



| <span data-ttu-id="95bd4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95bd4-120">Requirement</span></span> | <span data-ttu-id="95bd4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="95bd4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95bd4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95bd4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95bd4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95bd4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95bd4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95bd4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95bd4-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95bd4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95bd4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="95bd4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95bd4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95bd4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bd4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95bd4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="95bd4-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="95bd4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95bd4-130">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="95bd4-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="95bd4-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="95bd4-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95bd4-132">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="95bd4-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 






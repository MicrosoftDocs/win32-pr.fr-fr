---
description: Avertit une application lorsque le traitement des candidats est terminé et que l’IME est sur le paragraphe de déplacer la fenêtre candidate. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524260"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="9880a-104">\_Code de notification SETCANDIDATEPOS IMN</span><span class="sxs-lookup"><span data-stu-id="9880a-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="9880a-105">Avertit une application lorsque le traitement des candidats est terminé et que l’IME est sur le paragraphe de déplacer la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="9880a-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="9880a-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9880a-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="9880a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9880a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9880a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9880a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9880a-109">Défini sur IMN \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="9880a-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="9880a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9880a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9880a-111">Indicateur de liste de candidats.</span><span class="sxs-lookup"><span data-stu-id="9880a-111">Candidate list flag.</span></span> <span data-ttu-id="9880a-112">Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la seconde, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9880a-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="9880a-113">Si un bit spécifié est 1, la fenêtre candidate correspondante va être déplacée.</span><span class="sxs-lookup"><span data-stu-id="9880a-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9880a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9880a-114">Return Value</span></span>

<span data-ttu-id="9880a-115">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9880a-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9880a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9880a-116">Remarks</span></span>

<span data-ttu-id="9880a-117">Une application doit traiter cette commande si elle affiche la fenêtre candidate elle-même.</span><span class="sxs-lookup"><span data-stu-id="9880a-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="9880a-118">La fenêtre IME déplace la fenêtre candidate lors du traitement de cette commande.</span><span class="sxs-lookup"><span data-stu-id="9880a-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="9880a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9880a-119">Requirements</span></span>



| <span data-ttu-id="9880a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9880a-120">Requirement</span></span> | <span data-ttu-id="9880a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9880a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9880a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9880a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9880a-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9880a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9880a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9880a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9880a-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9880a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9880a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9880a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9880a-127"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9880a-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9880a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9880a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9880a-129">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9880a-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9880a-130">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9880a-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9880a-131">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="9880a-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





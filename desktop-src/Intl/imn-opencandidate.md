---
description: Avertit une application lorsqu’un IME est sur le paragraphe d’ouvrir la fenêtre candidate. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Événement IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865493"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="66dd3-104">\_Événement IMN OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="66dd3-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="66dd3-105">Avertit une application lorsqu’un IME est sur le paragraphe d’ouvrir la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="66dd3-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="66dd3-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="66dd3-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="66dd3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66dd3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66dd3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="66dd3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="66dd3-109">Défini sur IMN \_ OPENCANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="66dd3-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="66dd3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="66dd3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="66dd3-111">Indicateur de liste de candidats.</span><span class="sxs-lookup"><span data-stu-id="66dd3-111">Candidate list flag.</span></span> <span data-ttu-id="66dd3-112">Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la seconde, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="66dd3-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="66dd3-113">Si un bit spécifié est 1, la fenêtre candidate correspondante est sur le lieu d’être ouverte.</span><span class="sxs-lookup"><span data-stu-id="66dd3-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66dd3-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="66dd3-114">Return Value</span></span>

<span data-ttu-id="66dd3-115">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="66dd3-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66dd3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="66dd3-116">Remarks</span></span>

<span data-ttu-id="66dd3-117">Une application doit traiter cette commande si elle affiche des candidats.</span><span class="sxs-lookup"><span data-stu-id="66dd3-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="66dd3-118">L’application peut récupérer une liste de candidats à afficher à l’aide de la fonction [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="66dd3-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="66dd3-119">Par défaut, la fenêtre IME crée une fenêtre candidate lors du traitement de cette commande.</span><span class="sxs-lookup"><span data-stu-id="66dd3-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dd3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66dd3-120">Requirements</span></span>



| <span data-ttu-id="66dd3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66dd3-121">Requirement</span></span> | <span data-ttu-id="66dd3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="66dd3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66dd3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66dd3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66dd3-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66dd3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="66dd3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66dd3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66dd3-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66dd3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66dd3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="66dd3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66dd3-128"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66dd3-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66dd3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66dd3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dd3-130">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="66dd3-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="66dd3-131">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="66dd3-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="66dd3-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="66dd3-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="66dd3-133">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="66dd3-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





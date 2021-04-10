---
description: Avertit l’application lorsqu’un IME est sur le paragraphe de modifier le contenu de la fenêtre candidate. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115623"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="f94fe-104">\_Code de notification CHANGECANDIDATE IMN</span><span class="sxs-lookup"><span data-stu-id="f94fe-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="f94fe-105">Avertit l’application lorsqu’un IME est sur le paragraphe de modifier le contenu de la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="f94fe-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="f94fe-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f94fe-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="f94fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f94fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94fe-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f94fe-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f94fe-109">Défini sur IMN \_ CHANGECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="f94fe-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="f94fe-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f94fe-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f94fe-111">Indicateur de liste de candidats.</span><span class="sxs-lookup"><span data-stu-id="f94fe-111">Candidate list flag.</span></span> <span data-ttu-id="f94fe-112">Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la deuxième liste, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f94fe-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="f94fe-113">Si un bit spécifié est 1, la fenêtre candidate correspondante va être modifiée.</span><span class="sxs-lookup"><span data-stu-id="f94fe-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94fe-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f94fe-114">Return Value</span></span>

<span data-ttu-id="f94fe-115">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f94fe-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94fe-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f94fe-116">Remarks</span></span>

<span data-ttu-id="f94fe-117">Une application doit traiter cette commande si elle affiche des candidats.</span><span class="sxs-lookup"><span data-stu-id="f94fe-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="f94fe-118">La fenêtre IME modifie l’apparence de la fenêtre candidate lors du traitement de cette commande.</span><span class="sxs-lookup"><span data-stu-id="f94fe-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="f94fe-119">Une application peut obtenir des informations sur la fenêtre système avec [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) et [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span><span class="sxs-lookup"><span data-stu-id="f94fe-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="f94fe-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f94fe-120">Requirements</span></span>



| <span data-ttu-id="f94fe-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f94fe-121">Requirement</span></span> | <span data-ttu-id="f94fe-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f94fe-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94fe-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f94fe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f94fe-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f94fe-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f94fe-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f94fe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f94fe-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f94fe-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f94fe-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f94fe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f94fe-128"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f94fe-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94fe-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f94fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94fe-130">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="f94fe-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f94fe-131">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="f94fe-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f94fe-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="f94fe-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="f94fe-133">**ImmGetCandidateListCount**</span><span class="sxs-lookup"><span data-stu-id="f94fe-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="f94fe-134">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="f94fe-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





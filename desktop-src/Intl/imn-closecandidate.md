---
description: Avertit une application lorsqu’un IME est sur le paragraphe de fermer la fenêtre candidats. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534294"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="8c2d2-104">\_Code de notification CLOSECANDIDATE IMN</span><span class="sxs-lookup"><span data-stu-id="8c2d2-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="8c2d2-105">Avertit une application lorsqu’un IME est sur le paragraphe de fermer la fenêtre candidats.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="8c2d2-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="8c2d2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c2d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2d2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c2d2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8c2d2-109">Défini sur IMN \_ CLOSECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="8c2d2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c2d2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8c2d2-111">Indicateur de liste de candidats.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-111">Candidate list flag.</span></span> <span data-ttu-id="8c2d2-112">Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la seconde, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="8c2d2-113">Si un bit spécifié est 1, la fenêtre candidats correspondante est sur le lieu d’être fermée.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2d2-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c2d2-114">Return Value</span></span>

<span data-ttu-id="8c2d2-115">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2d2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8c2d2-116">Remarks</span></span>

<span data-ttu-id="8c2d2-117">Une application doit traiter cette commande si elle affiche des candidats.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="8c2d2-118">Par défaut, la fenêtre IME détruit une fenêtre candidate lors du traitement de cette commande.</span><span class="sxs-lookup"><span data-stu-id="8c2d2-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2d2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c2d2-119">Requirements</span></span>



| <span data-ttu-id="8c2d2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c2d2-120">Requirement</span></span> | <span data-ttu-id="8c2d2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c2d2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2d2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2d2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2d2-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c2d2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8c2d2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2d2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2d2-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c2d2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8c2d2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c2d2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c2d2-127"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c2d2-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2d2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2d2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2d2-129">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8c2d2-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8c2d2-130">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8c2d2-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="8c2d2-131">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="8c2d2-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





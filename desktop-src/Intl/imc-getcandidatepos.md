---
description: Demande à une fenêtre IME d’afficher la position de la fenêtre candidate. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Commande IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527012"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="93744-104">\_Commande IMC GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="93744-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="93744-105">Demande à une fenêtre IME d’afficher la position de la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="93744-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="93744-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="93744-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="93744-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93744-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93744-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="93744-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="93744-109">Défini sur IMC \_ GETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="93744-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="93744-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="93744-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="93744-111">Pointeur vers une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) qui contient la position de la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="93744-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93744-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="93744-112">Return Value</span></span>

<span data-ttu-id="93744-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="93744-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93744-114">Notes</span><span class="sxs-lookup"><span data-stu-id="93744-114">Remarks</span></span>

<span data-ttu-id="93744-115">Étant donné que l’IME peut ajuster la position d’une fenêtre candidate, une application utilise cette commande pour obtenir la position réelle pour décider s’il faut repositionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="93744-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="93744-116">La position Récupérée est dans les coordonnées de la fenêtre par rapport à la fenêtre qui a le focus d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="93744-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="93744-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93744-117">Requirements</span></span>



| <span data-ttu-id="93744-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93744-118">Requirement</span></span> | <span data-ttu-id="93744-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="93744-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93744-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93744-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93744-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93744-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="93744-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93744-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93744-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93744-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93744-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="93744-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93744-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93744-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93744-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93744-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93744-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="93744-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="93744-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="93744-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="93744-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="93744-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 





---
description: Notfies une application quand un IME sélectionné a besoin d’informations sur la fenêtre candidate. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529822"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="a4ccc-104">\_Code de notification IMR CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="a4ccc-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="a4ccc-105">Notfies une application quand un IME sélectionné a besoin d’informations sur la fenêtre candidate.</span><span class="sxs-lookup"><span data-stu-id="a4ccc-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="a4ccc-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a4ccc-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="a4ccc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4ccc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ccc-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4ccc-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a4ccc-109">Définissez sur IMR \_ CANDIDATEWINDOW.</span><span class="sxs-lookup"><span data-stu-id="a4ccc-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="a4ccc-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4ccc-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a4ccc-111">Pointeur vers une mémoire tampon contenant une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="a4ccc-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="a4ccc-112">Son membre **dwIndex** contient l’index de la fenêtre candidate référencée.</span><span class="sxs-lookup"><span data-stu-id="a4ccc-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ccc-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a4ccc-113">Return Value</span></span>

<span data-ttu-id="a4ccc-114">Retourne une valeur différente de zéro si l’application remplit la structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="a4ccc-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="a4ccc-115">Dans le cas contraire, la commande retourne 0.</span><span class="sxs-lookup"><span data-stu-id="a4ccc-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4ccc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a4ccc-116">Remarks</span></span>

<span data-ttu-id="a4ccc-117">Cette commande peut être envoyée par l’IME à une fenêtre qui a effacé l' \_ indicateur ISC SHOWUICANDIDATEWINDOW dans le gestionnaire de messages [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="a4ccc-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ccc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4ccc-118">Requirements</span></span>



| <span data-ttu-id="a4ccc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4ccc-119">Requirement</span></span> | <span data-ttu-id="a4ccc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4ccc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ccc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4ccc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ccc-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4ccc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a4ccc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4ccc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ccc-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4ccc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a4ccc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4ccc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4ccc-126"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4ccc-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ccc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4ccc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ccc-128">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="a4ccc-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a4ccc-129">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="a4ccc-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a4ccc-130">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="a4ccc-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="a4ccc-131">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="a4ccc-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="a4ccc-132">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a4ccc-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





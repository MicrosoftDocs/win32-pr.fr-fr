---
description: Avertit une application quand un IME sélectionné a besoin d’informations sur la fenêtre de composition. L’application reçoit cette commande via le \_ message de \_ demande de l’IME WM avec les paramètres définis comme indiqué ci-dessous.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533876"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="b5609-104">\_Code de notification IMR COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="b5609-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="b5609-105">Avertit une application quand un IME sélectionné a besoin d’informations sur la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="b5609-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="b5609-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres définis comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b5609-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="b5609-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5609-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5609-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5609-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b5609-109">Définissez sur IMR \_ COMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="b5609-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="b5609-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5609-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b5609-111">Pointeur vers une mémoire tampon contenant une structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="b5609-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5609-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5609-112">Return Value</span></span>

<span data-ttu-id="b5609-113">Retourne une valeur différente de zéro si l’application remplit la structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="b5609-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="b5609-114">Dans le cas contraire, la commande retourne 0.</span><span class="sxs-lookup"><span data-stu-id="b5609-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5609-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b5609-115">Remarks</span></span>

<span data-ttu-id="b5609-116">Cette commande peut être envoyée par l’IME à une fenêtre qui a effacé l' \_ indicateur ISC SHOWUICOMPOSITIONWINDOW dans le gestionnaire de messages [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="b5609-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5609-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5609-117">Requirements</span></span>



| <span data-ttu-id="b5609-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5609-118">Requirement</span></span> | <span data-ttu-id="b5609-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5609-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5609-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5609-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5609-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5609-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5609-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5609-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5609-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5609-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5609-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5609-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5609-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5609-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5609-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5609-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5609-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b5609-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b5609-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b5609-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b5609-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="b5609-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="b5609-130">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="b5609-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="b5609-131">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="b5609-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





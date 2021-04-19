---
description: Avertit une application quand un IME sélectionné a besoin d’informations sur la police utilisée par la fenêtre de composition. L’application reçoit cette commande via le \_ message de \_ requête de l’IME WM avec les paramètres, comme indiqué ci-dessous.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527877"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="803d8-104">\_Code de notification IMR COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="803d8-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="803d8-105">Avertit une application quand un IME sélectionné a besoin d’informations sur la police utilisée par la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="803d8-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="803d8-106">L’application reçoit cette commande via le message de [**\_ \_ requête de l’IME WM**](wm-ime-request.md) avec les paramètres, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="803d8-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="803d8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="803d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803d8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="803d8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="803d8-109">Définissez sur IMR \_ COMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="803d8-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="803d8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="803d8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="803d8-111">Pointeur vers une mémoire tampon contenant une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="803d8-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="803d8-112">L’application remplit les valeurs de la fenêtre de composition actuelle.</span><span class="sxs-lookup"><span data-stu-id="803d8-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803d8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="803d8-113">Return Value</span></span>

<span data-ttu-id="803d8-114">Retourne une valeur différente de zéro si l’application remplit la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="803d8-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="803d8-115">Dans le cas contraire, la commande retourne 0.</span><span class="sxs-lookup"><span data-stu-id="803d8-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="803d8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="803d8-116">Remarks</span></span>

<span data-ttu-id="803d8-117">Cette commande peut être envoyée par l’IME à une fenêtre qui a effacé l' \_ indicateur ISC SHOWUICOMPOSITIONWINDOW dans le gestionnaire de messages [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="803d8-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="803d8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="803d8-118">Requirements</span></span>



| <span data-ttu-id="803d8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="803d8-119">Requirement</span></span> | <span data-ttu-id="803d8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="803d8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="803d8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="803d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="803d8-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="803d8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="803d8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="803d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="803d8-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="803d8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="803d8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="803d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="803d8-126"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="803d8-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803d8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="803d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803d8-128">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="803d8-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="803d8-129">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="803d8-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="803d8-130">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="803d8-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="803d8-131">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="803d8-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 

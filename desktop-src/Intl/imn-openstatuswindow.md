---
description: Avertit une application lorsqu’un IME est sur le paragraphe de créer la fenêtre d’État. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531975"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="2b28d-104">\_Code de notification OPENSTATUSWINDOW IMN</span><span class="sxs-lookup"><span data-stu-id="2b28d-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="2b28d-105">Avertit une application lorsqu’un IME est sur le paragraphe de créer la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="2b28d-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="2b28d-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2b28d-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="2b28d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b28d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b28d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b28d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2b28d-109">Défini sur IMN \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="2b28d-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="2b28d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b28d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2b28d-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2b28d-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b28d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b28d-112">Return Value</span></span>

<span data-ttu-id="2b28d-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2b28d-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b28d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2b28d-114">Remarks</span></span>

<span data-ttu-id="2b28d-115">Une application traite cette commande pour afficher la fenêtre d’état de l’IME en soi.</span><span class="sxs-lookup"><span data-stu-id="2b28d-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="2b28d-116">La fenêtre IME crée une fenêtre d’état lors du traitement de cette commande et définit les chaînes à afficher dans la fenêtre dans le contexte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2b28d-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="2b28d-117">Les applications peuvent obtenir des informations sur la fenêtre d’État à l’aide de la fonction [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="2b28d-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b28d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b28d-118">Requirements</span></span>



| <span data-ttu-id="2b28d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b28d-119">Requirement</span></span> | <span data-ttu-id="2b28d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b28d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b28d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b28d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b28d-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b28d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2b28d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b28d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b28d-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b28d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2b28d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b28d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b28d-126"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b28d-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b28d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b28d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b28d-128">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b28d-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2b28d-129">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b28d-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2b28d-130">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="2b28d-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="2b28d-131">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="2b28d-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





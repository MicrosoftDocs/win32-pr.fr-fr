---
description: Avertit une application lorsqu’un IME est sur le paragraphe d’afficher un message d’erreur ou d’autres informations. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319282"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="942ac-104">Code de notification de l' \_ instruction IMN</span><span class="sxs-lookup"><span data-stu-id="942ac-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="942ac-105">Avertit une application lorsqu’un IME est sur le paragraphe d’afficher un message d’erreur ou d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="942ac-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="942ac-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="942ac-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="942ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="942ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="942ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="942ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="942ac-109">Défini sur IMN \_ Guideline.</span><span class="sxs-lookup"><span data-stu-id="942ac-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="942ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="942ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="942ac-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="942ac-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="942ac-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="942ac-112">Return Value</span></span>

<span data-ttu-id="942ac-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="942ac-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="942ac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="942ac-114">Remarks</span></span>

<span data-ttu-id="942ac-115">Une application traite cette commande en appelant la fonction [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) pour récupérer le message d’erreur ou les informations de l’IME.</span><span class="sxs-lookup"><span data-stu-id="942ac-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="942ac-116">La fenêtre IME affiche le message d’erreur ou la chaîne d’informations dans une fenêtre d’informations.</span><span class="sxs-lookup"><span data-stu-id="942ac-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="942ac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="942ac-117">Requirements</span></span>



| <span data-ttu-id="942ac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="942ac-118">Requirement</span></span> | <span data-ttu-id="942ac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="942ac-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="942ac-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="942ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="942ac-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="942ac-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="942ac-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="942ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="942ac-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="942ac-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="942ac-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="942ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="942ac-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="942ac-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="942ac-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="942ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942ac-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="942ac-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="942ac-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="942ac-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="942ac-129">**ImmGetGuideLine**</span><span class="sxs-lookup"><span data-stu-id="942ac-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="942ac-130">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="942ac-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





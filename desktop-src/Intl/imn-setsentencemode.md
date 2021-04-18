---
description: Avertit une application lorsque le mode de phrase du contexte d’entrée est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: IMN_SETSENTENCEMODE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0130c5b3d7284112e64cca698b358650f51f3642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536366"
---
# <a name="imn_setsentencemode-notification-code"></a><span data-ttu-id="e2d14-104">\_Code de notification SETSENTENCEMODE IMN</span><span class="sxs-lookup"><span data-stu-id="e2d14-104">IMN\_SETSENTENCEMODE notification code</span></span>

<span data-ttu-id="e2d14-105">Avertit une application lorsque le mode de phrase du contexte d’entrée est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e2d14-105">Notifies an application when the sentence mode of the input context is updated.</span></span> <span data-ttu-id="e2d14-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e2d14-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a><span data-ttu-id="e2d14-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2d14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d14-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2d14-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e2d14-109">Défini sur IMN \_ SETSENTENCEMODE.</span><span class="sxs-lookup"><span data-stu-id="e2d14-109">Set to IMN\_SETSENTENCEMODE.</span></span>

</dd> <dt>

<span data-ttu-id="e2d14-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2d14-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e2d14-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e2d14-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d14-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2d14-112">Return Value</span></span>

<span data-ttu-id="e2d14-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e2d14-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d14-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e2d14-114">Remarks</span></span>

<span data-ttu-id="e2d14-115">L’application peut obtenir des informations sur le mode phrase à l’aide de la fonction [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e2d14-115">The application can get information about the sentence mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d14-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2d14-116">Requirements</span></span>



| <span data-ttu-id="e2d14-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2d14-117">Requirement</span></span> | <span data-ttu-id="e2d14-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2d14-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d14-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2d14-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d14-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2d14-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2d14-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2d14-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d14-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2d14-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2d14-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2d14-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d14-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d14-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d14-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2d14-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d14-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="e2d14-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e2d14-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="e2d14-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e2d14-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d14-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="e2d14-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="e2d14-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





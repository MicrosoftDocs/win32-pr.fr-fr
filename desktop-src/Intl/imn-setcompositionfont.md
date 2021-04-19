---
description: Avertit une application lorsque la police du contexte d’entrée est mise à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544308"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="ee40a-104">\_Code de notification SETCOMPOSITIONFONT IMN</span><span class="sxs-lookup"><span data-stu-id="ee40a-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="ee40a-105">Avertit une application lorsque la police du contexte d’entrée est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ee40a-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="ee40a-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ee40a-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="ee40a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee40a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee40a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee40a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ee40a-109">Défini sur IMN \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="ee40a-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="ee40a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee40a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ee40a-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ee40a-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee40a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee40a-112">Return Value</span></span>

<span data-ttu-id="ee40a-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ee40a-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee40a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ee40a-114">Remarks</span></span>

<span data-ttu-id="ee40a-115">L’application peut obtenir des informations sur la police à l’aide de la fonction [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) .</span><span class="sxs-lookup"><span data-stu-id="ee40a-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="ee40a-116">La fenêtre IME utilise ensuite la police pour dessiner la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="ee40a-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee40a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee40a-117">Requirements</span></span>



| <span data-ttu-id="ee40a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee40a-118">Requirement</span></span> | <span data-ttu-id="ee40a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee40a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee40a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee40a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee40a-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee40a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee40a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee40a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee40a-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee40a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee40a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee40a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee40a-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee40a-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee40a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee40a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee40a-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="ee40a-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ee40a-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="ee40a-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ee40a-129">**ImmGetCompositionFont**</span><span class="sxs-lookup"><span data-stu-id="ee40a-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="ee40a-130">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="ee40a-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





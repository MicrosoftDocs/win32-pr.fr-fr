---
description: Avertit une application lorsque le mode de conversion du contexte d’entrée est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: IMN_SETCONVERSIONMODE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526236"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="7145e-104">\_Code de notification SETCONVERSIONMODE IMN</span><span class="sxs-lookup"><span data-stu-id="7145e-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="7145e-105">Avertit une application lorsque le mode de conversion du contexte d’entrée est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7145e-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="7145e-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7145e-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="7145e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7145e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7145e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7145e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7145e-109">Défini sur IMN \_ SETCONVERSIONMODE.</span><span class="sxs-lookup"><span data-stu-id="7145e-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="7145e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7145e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7145e-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7145e-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7145e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7145e-112">Return Value</span></span>

<span data-ttu-id="7145e-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7145e-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7145e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7145e-114">Remarks</span></span>

<span data-ttu-id="7145e-115">L’application peut obtenir des informations sur le mode de conversion à l’aide de la fonction [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="7145e-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7145e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7145e-116">Requirements</span></span>



| <span data-ttu-id="7145e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7145e-117">Requirement</span></span> | <span data-ttu-id="7145e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7145e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7145e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7145e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7145e-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7145e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7145e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7145e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7145e-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7145e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7145e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7145e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7145e-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7145e-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7145e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7145e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7145e-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7145e-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7145e-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7145e-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7145e-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="7145e-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="7145e-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="7145e-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





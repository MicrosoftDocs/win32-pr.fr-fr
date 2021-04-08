---
description: Avertit une application lorsque l’état ouvert du contexte d’entrée est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034490"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="0925b-104">\_Code de notification SETOPENSTATUS IMN</span><span class="sxs-lookup"><span data-stu-id="0925b-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="0925b-105">Avertit une application lorsque l’état ouvert du contexte d’entrée est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0925b-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="0925b-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0925b-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="0925b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0925b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0925b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="0925b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="0925b-109">Défini sur IMN \_ SETOPENSTATUS.</span><span class="sxs-lookup"><span data-stu-id="0925b-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="0925b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0925b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0925b-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0925b-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0925b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0925b-112">Return Value</span></span>

<span data-ttu-id="0925b-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="0925b-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0925b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0925b-114">Remarks</span></span>

<span data-ttu-id="0925b-115">L’application peut obtenir des informations sur l’état ouvert à l’aide de la fonction [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .</span><span class="sxs-lookup"><span data-stu-id="0925b-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0925b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0925b-116">Requirements</span></span>



| <span data-ttu-id="0925b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0925b-117">Requirement</span></span> | <span data-ttu-id="0925b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0925b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0925b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0925b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0925b-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0925b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0925b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0925b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0925b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0925b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0925b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0925b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0925b-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0925b-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0925b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0925b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0925b-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="0925b-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="0925b-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="0925b-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="0925b-128">**ImmGetOpenStatus**</span><span class="sxs-lookup"><span data-stu-id="0925b-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="0925b-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="0925b-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





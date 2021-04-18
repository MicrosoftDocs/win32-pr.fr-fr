---
description: Avertit une application lorsque la position de la fenêtre d’État dans le contexte d’entrée est mise à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre comme suit.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: IMN_SETSTATUSWINDOWPOS le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519884"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="789cb-104">\_Code de notification SETSTATUSWINDOWPOS IMN</span><span class="sxs-lookup"><span data-stu-id="789cb-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="789cb-105">Avertit une application lorsque la position de la fenêtre d’État dans le contexte d’entrée est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="789cb-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="789cb-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre comme suit.</span><span class="sxs-lookup"><span data-stu-id="789cb-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="789cb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="789cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789cb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="789cb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="789cb-109">Défini sur IMN \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="789cb-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="789cb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="789cb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="789cb-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="789cb-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789cb-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="789cb-112">Return Value</span></span>

<span data-ttu-id="789cb-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="789cb-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="789cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="789cb-114">Remarks</span></span>

<span data-ttu-id="789cb-115">L’application peut obtenir des informations sur la position de la fenêtre d’État à l’aide de la commande [**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) .</span><span class="sxs-lookup"><span data-stu-id="789cb-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="789cb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="789cb-116">Requirements</span></span>



| <span data-ttu-id="789cb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="789cb-117">Requirement</span></span> | <span data-ttu-id="789cb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="789cb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789cb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="789cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="789cb-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="789cb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="789cb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="789cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="789cb-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="789cb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="789cb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="789cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="789cb-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="789cb-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789cb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="789cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789cb-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="789cb-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="789cb-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="789cb-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="789cb-128">**\_GETSTATUSWINDOWPOS IMC**</span><span class="sxs-lookup"><span data-stu-id="789cb-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="789cb-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="789cb-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





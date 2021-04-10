---
description: Avertit une application lorsque le style ou la position de la fenêtre de composition est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952814"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="9a97c-104">\_Code de notification SETCOMPOSITIONWINDOW IMN</span><span class="sxs-lookup"><span data-stu-id="9a97c-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="9a97c-105">Avertit une application lorsque le style ou la position de la fenêtre de composition est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9a97c-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="9a97c-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9a97c-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="9a97c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a97c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a97c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a97c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9a97c-109">Défini sur IMN \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="9a97c-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="9a97c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a97c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9a97c-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9a97c-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a97c-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a97c-112">Return Value</span></span>

<span data-ttu-id="9a97c-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9a97c-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a97c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9a97c-114">Remarks</span></span>

<span data-ttu-id="9a97c-115">L’application peut obtenir des informations sur le formulaire de composition à l’aide de la commande [**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="9a97c-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a97c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a97c-116">Requirements</span></span>



| <span data-ttu-id="9a97c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a97c-117">Requirement</span></span> | <span data-ttu-id="9a97c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a97c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a97c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a97c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a97c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a97c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a97c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a97c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a97c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a97c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a97c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a97c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a97c-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a97c-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a97c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a97c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a97c-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9a97c-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9a97c-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9a97c-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9a97c-128">**\_GETCOMPOSITIONWINDOW IMC**</span><span class="sxs-lookup"><span data-stu-id="9a97c-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="9a97c-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="9a97c-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





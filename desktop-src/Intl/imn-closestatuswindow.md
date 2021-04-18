---
description: Avertit une application quand un IME est sur le paragraphe de fermer la fenêtre d’État. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533915"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="877d8-104">\_Code de notification CLOSESTATUSWINDOW IMN</span><span class="sxs-lookup"><span data-stu-id="877d8-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="877d8-105">Avertit une application quand un IME est sur le paragraphe de fermer la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="877d8-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="877d8-106">L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="877d8-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="877d8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="877d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="877d8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="877d8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="877d8-109">Défini sur IMN \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="877d8-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="877d8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="877d8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="877d8-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="877d8-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="877d8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="877d8-112">Return Value</span></span>

<span data-ttu-id="877d8-113">Cette commande n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="877d8-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="877d8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="877d8-114">Remarks</span></span>

<span data-ttu-id="877d8-115">Une application doit traiter cette commande si elle affiche la fenêtre d’état de l’IME.</span><span class="sxs-lookup"><span data-stu-id="877d8-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="877d8-116">La fenêtre IME ferme la fenêtre d’état lors du traitement de cette commande.</span><span class="sxs-lookup"><span data-stu-id="877d8-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="877d8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="877d8-117">Requirements</span></span>



| <span data-ttu-id="877d8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="877d8-118">Requirement</span></span> | <span data-ttu-id="877d8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="877d8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877d8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="877d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="877d8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="877d8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="877d8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="877d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="877d8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="877d8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="877d8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="877d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="877d8-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="877d8-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="877d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="877d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877d8-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="877d8-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="877d8-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="877d8-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="877d8-129">**notification de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="877d8-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





---
description: Utilisé pour définir des messages privés, généralement sous la forme WM \_ app + x, où x est une valeur entière.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203801"
---
# <a name="wm_app"></a><span data-ttu-id="f704b-103">\_application WM</span><span class="sxs-lookup"><span data-stu-id="f704b-103">WM\_APP</span></span>

<span data-ttu-id="f704b-104">Utilisé pour définir des messages privés, généralement au format **WM \_ app** + *x*, où *x* est une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="f704b-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="f704b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f704b-105">Remarks</span></span>

<span data-ttu-id="f704b-106">La constante d' **\_ application WM** est utilisée pour faire la distinction entre les valeurs de message qui sont réservées à une utilisation par le système et les valeurs qui peuvent être utilisées par une application pour envoyer des messages dans une classe de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="f704b-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="f704b-107">Voici les plages de numéros de message disponibles.</span><span class="sxs-lookup"><span data-stu-id="f704b-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="f704b-108">Plage</span><span class="sxs-lookup"><span data-stu-id="f704b-108">Range</span></span>                                                 | <span data-ttu-id="f704b-109">Signification</span><span class="sxs-lookup"><span data-stu-id="f704b-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f704b-110">0 à [**\_ utilisateur WM**](wm-user.md) – 1</span><span class="sxs-lookup"><span data-stu-id="f704b-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="f704b-111">Messages réservés pour une utilisation par le système.</span><span class="sxs-lookup"><span data-stu-id="f704b-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="f704b-112">[**WM \_ UTILISATEUR**](wm-user.md) via 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="f704b-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="f704b-113">Messages entiers à utiliser par les classes de fenêtre privées.</span><span class="sxs-lookup"><span data-stu-id="f704b-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="f704b-114">**WM \_ APPLICATION** via 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="f704b-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="f704b-115">Messages disponibles pour une utilisation par des applications.</span><span class="sxs-lookup"><span data-stu-id="f704b-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="f704b-116">0xC000 à 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="f704b-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="f704b-117">Messages de chaîne à utiliser par les applications.</span><span class="sxs-lookup"><span data-stu-id="f704b-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="f704b-118">Supérieur à 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="f704b-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="f704b-119">Réservé par le système.</span><span class="sxs-lookup"><span data-stu-id="f704b-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="f704b-120">Les numéros de message dans la première plage (0 à [**\_ utilisateur WM**](wm-user.md) – 1) sont définis par le système.</span><span class="sxs-lookup"><span data-stu-id="f704b-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="f704b-121">Les valeurs de cette plage qui ne sont pas définies explicitement sont réservées par le système.</span><span class="sxs-lookup"><span data-stu-id="f704b-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="f704b-122">Les numéros de message dans la deuxième plage ([**\_ utilisateur WM**](wm-user.md) via 0x7FFF) peuvent être définis et utilisés par une application pour envoyer des messages dans une classe de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="f704b-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="f704b-123">Ces valeurs ne peuvent pas être utilisées pour définir des messages significatifs dans une application, car certaines classes de fenêtres prédéfinies définissent déjà des valeurs dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="f704b-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="f704b-124">Par exemple, les classes de contrôle prédéfinies telles que **Button**, **Edit**, **ListBox** et **ComboBox** peuvent utiliser ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f704b-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="f704b-125">Les messages de cette plage ne doivent pas être envoyés à d’autres applications, sauf si les applications ont été conçues pour échanger des messages et pour attacher la même signification aux numéros de message.</span><span class="sxs-lookup"><span data-stu-id="f704b-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="f704b-126">Les numéros de message dans la troisième plage (0x8000 à 0xBFFF) sont disponibles pour les applications à utiliser comme messages privés.</span><span class="sxs-lookup"><span data-stu-id="f704b-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="f704b-127">Les messages de cette plage ne sont pas en conflit avec les messages système.</span><span class="sxs-lookup"><span data-stu-id="f704b-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="f704b-128">Les numéros de message dans la quatrième plage (0xC000 à 0xFFFF) sont définis au moment de l’exécution lorsqu’une application appelle la fonction [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) pour récupérer un numéro de message pour une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f704b-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="f704b-129">Toutes les applications qui inscrivent la même chaîne peuvent utiliser le numéro de message associé à l’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="f704b-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="f704b-130">Toutefois, le numéro de message réel n’est pas une constante et ne peut pas être utilisé de la même façon entre différentes sessions.</span><span class="sxs-lookup"><span data-stu-id="f704b-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="f704b-131">Les numéros de message dans la cinquième plage (supérieure à 0xFFFF) sont réservés par le système.</span><span class="sxs-lookup"><span data-stu-id="f704b-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="f704b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f704b-132">Requirements</span></span>



| <span data-ttu-id="f704b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f704b-133">Requirement</span></span> | <span data-ttu-id="f704b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f704b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f704b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f704b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f704b-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f704b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f704b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f704b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f704b-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f704b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f704b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="f704b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f704b-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f704b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f704b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f704b-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="f704b-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f704b-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f704b-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="f704b-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="f704b-144">**\_utilisateur WM**</span><span class="sxs-lookup"><span data-stu-id="f704b-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="f704b-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f704b-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f704b-146">Messages et files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="f704b-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 

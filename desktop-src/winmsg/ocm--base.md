---
description: Utilisé pour définir des messages privés pour une utilisation par les classes de fenêtre privées, généralement sous la forme OCM \_ \_ base + x, où x est une valeur entière.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (OLECTL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588062"
---
# <a name="ocm__base"></a><span data-ttu-id="efaf2-103">BASE de OCM \_ \_</span><span class="sxs-lookup"><span data-stu-id="efaf2-103">OCM\_\_BASE</span></span>

<span data-ttu-id="efaf2-104">Utilisé pour définir des messages privés pour une utilisation par les classes de fenêtre privées, généralement sous la forme **OCM \_ \_ base** + *x*, où *x* est une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="efaf2-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="efaf2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="efaf2-105">Remarks</span></span>

<span data-ttu-id="efaf2-106">Voici les plages de numéros de message.</span><span class="sxs-lookup"><span data-stu-id="efaf2-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="efaf2-107">Plage</span><span class="sxs-lookup"><span data-stu-id="efaf2-107">Range</span></span>                                                 | <span data-ttu-id="efaf2-108">Signification</span><span class="sxs-lookup"><span data-stu-id="efaf2-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="efaf2-109">0 à [**l' \_ utilisateur WM**](wm-user.md)-1</span><span class="sxs-lookup"><span data-stu-id="efaf2-109">0 through [**WM\_USER**](wm-user.md)-1</span></span><br/>   | <span data-ttu-id="efaf2-110">Messages réservés pour une utilisation par le système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="efaf2-111">[**WM \_ UTILISATEUR**](wm-user.md) via 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="efaf2-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="efaf2-112">Messages entiers à utiliser par les classes de fenêtre privées.</span><span class="sxs-lookup"><span data-stu-id="efaf2-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="efaf2-113">[**WM \_ APPLICATION**](wm-app.md) via 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="efaf2-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="efaf2-114">Messages disponibles pour une utilisation par des applications.</span><span class="sxs-lookup"><span data-stu-id="efaf2-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="efaf2-115">0xC000 à 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="efaf2-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="efaf2-116">Messages de chaîne à utiliser par les applications.</span><span class="sxs-lookup"><span data-stu-id="efaf2-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="efaf2-117">Supérieur à 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="efaf2-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="efaf2-118">Réservé par le système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="efaf2-119">Les numéros de message dans la première plage (0 à [**WM \_ utilisateur**](wm-user.md)  1) sont définis par le système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="efaf2-120">Les valeurs de cette plage qui ne sont pas définies explicitement sont réservées par le système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="efaf2-121">Les numéros de message dans la deuxième plage ([**\_ utilisateur WM**](wm-user.md) via 0x7FFF) peuvent être définis et utilisés par une application pour envoyer des messages dans une classe de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="efaf2-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="efaf2-122">Ces valeurs ne peuvent pas être utilisées pour définir des messages significatifs dans une application, car certaines classes de fenêtres prédéfinies définissent déjà des valeurs dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="efaf2-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="efaf2-123">Par exemple, les classes de contrôle prédéfinies telles que **Button**, **Edit**, **ListBox** et **ComboBox** peuvent utiliser ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="efaf2-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="efaf2-124">Les messages de cette plage ne doivent pas être envoyés à d’autres applications, sauf si les applications ont été conçues pour échanger des messages et pour attacher la même signification aux numéros de message.</span><span class="sxs-lookup"><span data-stu-id="efaf2-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="efaf2-125">Les numéros de message dans la troisième plage (0x8000 à 0xBFFF) sont disponibles pour les applications à utiliser comme messages privés.</span><span class="sxs-lookup"><span data-stu-id="efaf2-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="efaf2-126">Les messages de cette plage ne sont pas en conflit avec les messages système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="efaf2-127">Les numéros de message dans la quatrième plage (0xC000 à 0xFFFF) sont définis au moment de l’exécution lorsqu’une application appelle la fonction [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) pour récupérer un numéro de message pour une chaîne.</span><span class="sxs-lookup"><span data-stu-id="efaf2-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="efaf2-128">Toutes les applications qui inscrivent la même chaîne peuvent utiliser le numéro de message associé à l’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="efaf2-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="efaf2-129">Toutefois, le numéro de message réel n’est pas une constante et ne peut pas être utilisé de la même façon entre différentes sessions.</span><span class="sxs-lookup"><span data-stu-id="efaf2-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="efaf2-130">Les numéros de message dans la cinquième plage (supérieure à 0xFFFF) sont réservés par le système.</span><span class="sxs-lookup"><span data-stu-id="efaf2-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="efaf2-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="efaf2-131">Requirements</span></span>



| <span data-ttu-id="efaf2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efaf2-132">Requirement</span></span> | <span data-ttu-id="efaf2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="efaf2-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="efaf2-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efaf2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efaf2-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efaf2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="efaf2-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efaf2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efaf2-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efaf2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="efaf2-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="efaf2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="efaf2-139"><dt>OLECTL. h</dt></span><span class="sxs-lookup"><span data-stu-id="efaf2-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efaf2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efaf2-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="efaf2-141">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="efaf2-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="efaf2-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="efaf2-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="efaf2-143">**\_application WM**</span><span class="sxs-lookup"><span data-stu-id="efaf2-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="efaf2-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="efaf2-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="efaf2-145">Messages et files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="efaf2-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 


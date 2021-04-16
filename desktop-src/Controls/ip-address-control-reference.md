---
title: Contrôle d’adresse IP
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’adresse IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462122"
---
# <a name="ip-address-control"></a><span data-ttu-id="1c8ad-103">Contrôle d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="1c8ad-103">IP Address Control</span></span>

<span data-ttu-id="1c8ad-104">Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="1c8ad-105">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="1c8ad-105">Overviews</span></span>



| <span data-ttu-id="1c8ad-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ad-106">Topic</span></span>                                          | <span data-ttu-id="1c8ad-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c8ad-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ad-108">Contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="1c8ad-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="1c8ad-109">Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="1c8ad-110">Macros</span><span class="sxs-lookup"><span data-stu-id="1c8ad-110">Macros</span></span>



| <span data-ttu-id="1c8ad-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ad-111">Topic</span></span>                                         | <span data-ttu-id="1c8ad-112">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c8ad-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ad-113">**PREMIÈRE \_ adresse IP**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="1c8ad-114">Extrait la valeur du champ 0 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="1c8ad-115">**QUATRIÈME \_ adresse IP**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="1c8ad-116">Extrait la valeur du champ 3 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="1c8ad-117">**MAKEIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="1c8ad-118">Compresse quatre valeurs d’octet en un seul LPARAM pouvant être utilisé avec le message [**IPM \_ SETADDRESS**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="1c8ad-119">**MAKEIPRANGE**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="1c8ad-120">Compresse deux valeurs d’octet en un seul LPARAM pouvant être utilisé avec le message [**IPM \_ SetRange**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="1c8ad-121">**DEUXIÈME \_ adresse IP**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="1c8ad-122">Extrait la valeur du champ 1 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="1c8ad-123">**TROISIÈME \_ adresse IP**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="1c8ad-124">Extrait la valeur du champ 2 d’une adresse IP compressée extraite avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="1c8ad-125">Messages</span><span class="sxs-lookup"><span data-stu-id="1c8ad-125">Messages</span></span>



| <span data-ttu-id="1c8ad-126">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ad-126">Topic</span></span>                                         | <span data-ttu-id="1c8ad-127">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c8ad-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ad-128">**\_CLEARADDRESS IPM**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="1c8ad-129">Efface le contenu du contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="1c8ad-130">**maipm, \_ GETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="1c8ad-131">Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="1c8ad-132">**\_ISBLANK IPM**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="1c8ad-133">Détermine si tous les champs du contrôle d’adresse IP sont vides.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="1c8ad-134">**\_SETADDRESS IPM**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="1c8ad-135">Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="1c8ad-136">**IPM \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="1c8ad-137">Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="1c8ad-138">Tout le texte de ce champ est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="1c8ad-139">**IPM \_ SEtrange**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="1c8ad-140">Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="1c8ad-141">Notifications</span><span class="sxs-lookup"><span data-stu-id="1c8ad-141">Notifications</span></span>



| <span data-ttu-id="1c8ad-142">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ad-142">Topic</span></span>                                     | <span data-ttu-id="1c8ad-143">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c8ad-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ad-144">IPN \_ FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="1c8ad-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="1c8ad-145">Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre.</span><span class="sxs-lookup"><span data-stu-id="1c8ad-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="1c8ad-146">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="1c8ad-147">Structures</span><span class="sxs-lookup"><span data-stu-id="1c8ad-147">Structures</span></span>



| <span data-ttu-id="1c8ad-148">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ad-148">Topic</span></span>                              | <span data-ttu-id="1c8ad-149">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c8ad-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ad-150">**NMIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1c8ad-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="1c8ad-151">Contient des informations pour le code de notification [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ad-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 






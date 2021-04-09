---
title: Contrôle Up-Down
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles Up-Up.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029047"
---
# <a name="up-down-control"></a><span data-ttu-id="85248-103">Contrôle Up-Down</span><span class="sxs-lookup"><span data-stu-id="85248-103">Up-Down Control</span></span>

<span data-ttu-id="85248-104">Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles Up-Up.</span><span class="sxs-lookup"><span data-stu-id="85248-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="85248-105">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="85248-105">Overviews</span></span>



| <span data-ttu-id="85248-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-106">Topic</span></span>                                    | <span data-ttu-id="85248-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-108">Contrôles Up-Up</span><span class="sxs-lookup"><span data-stu-id="85248-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="85248-109">Un contrôle up-up est une paire de boutons fléchés sur lesquels l’utilisateur peut cliquer pour incrémenter ou décrémenter une valeur, telle qu’une position de défilement ou un nombre affiché dans un contrôle auxiliaire (appelé fenêtre associée).</span><span class="sxs-lookup"><span data-stu-id="85248-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="85248-110">Fonctions</span><span class="sxs-lookup"><span data-stu-id="85248-110">Functions</span></span>



| <span data-ttu-id="85248-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-111">Topic</span></span>                                              | <span data-ttu-id="85248-112">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-113">**CreateUpDownControl**</span><span class="sxs-lookup"><span data-stu-id="85248-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="85248-114">Crée un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-114">Creates an up-down control.</span></span> <span data-ttu-id="85248-115">Remarque : cette fonction est obsolète.</span><span class="sxs-lookup"><span data-stu-id="85248-115">Note: This function is obsolete.</span></span> <span data-ttu-id="85248-116">Il s’agit d’une fonction 16 bits qui ne peut pas gérer les valeurs 32 bits pour la plage et la position.</span><span class="sxs-lookup"><span data-stu-id="85248-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="85248-117">Messages</span><span class="sxs-lookup"><span data-stu-id="85248-117">Messages</span></span>



| <span data-ttu-id="85248-118">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-118">Topic</span></span>                                                 | <span data-ttu-id="85248-119">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-120">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="85248-121">Récupère les informations d’accélération pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="85248-122">**\_GETBASE (UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="85248-123">Récupère la base de la base actuelle (c’est-à-dire, base 10 ou 16) pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="85248-124">**\_GETBUDDY UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="85248-125">Récupère le handle de la fenêtre associée actuelle.</span><span class="sxs-lookup"><span data-stu-id="85248-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="85248-126">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="85248-127">Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="85248-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="85248-128">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="85248-129">Retourne la position 32 bits d’un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="85248-130">**\_GETRANGE UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="85248-131">Récupère les positions minimale et maximale (plage) pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="85248-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="85248-133">Récupère la plage 32 bits d’un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="85248-134">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="85248-135">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="85248-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="85248-136">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="85248-137">Définit l’accélération pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="85248-138">**\_SETBASE UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="85248-139">Définit la base de base pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="85248-140">La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="85248-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="85248-141">Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés.</span><span class="sxs-lookup"><span data-stu-id="85248-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="85248-142">**\_SETBUDDY UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="85248-143">Définit la fenêtre associée pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="85248-144">**\_SetPos UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="85248-145">Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="85248-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="85248-146">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="85248-147">Définit la position d’un contrôle up-up avec une précision de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85248-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="85248-148">**e \_ trange UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="85248-149">Définit les positions minimale et maximale (plage) pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="85248-150">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="85248-151">Définit la plage de bits 32 d’un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="85248-152">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="85248-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="85248-153">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="85248-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="85248-154">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="85248-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="85248-155">Notifications</span><span class="sxs-lookup"><span data-stu-id="85248-155">Notifications</span></span>



| <span data-ttu-id="85248-156">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-156">Topic</span></span>                                                            | <span data-ttu-id="85248-157">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-158">NM \_ RELEASEDCAPTURE (Up-Up)</span><span class="sxs-lookup"><span data-stu-id="85248-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="85248-159">Avertit une fenêtre parente d’un contrôle up-up que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="85248-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="85248-160">Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="85248-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="85248-161">UDN \_ DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="85248-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="85248-162">Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée.</span><span class="sxs-lookup"><span data-stu-id="85248-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="85248-163">Cela se produit lorsque l’utilisateur demande une modification de la valeur en appuyant sur la flèche haut ou bas du contrôle.</span><span class="sxs-lookup"><span data-stu-id="85248-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="85248-164">Le message [UDN \_ DELTAPOS](udn-deltapos.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="85248-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="85248-165">Structures</span><span class="sxs-lookup"><span data-stu-id="85248-165">Structures</span></span>



| <span data-ttu-id="85248-166">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-166">Topic</span></span>                        | <span data-ttu-id="85248-167">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-168">**NMUPDOWN**</span><span class="sxs-lookup"><span data-stu-id="85248-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="85248-169">Contient des informations spécifiques aux messages de notification de contrôle up-out.</span><span class="sxs-lookup"><span data-stu-id="85248-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="85248-170">Elle est identique à et remplace la structure de **\_ déverrouillage nm** .</span><span class="sxs-lookup"><span data-stu-id="85248-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="85248-171">**UDACCEL**</span><span class="sxs-lookup"><span data-stu-id="85248-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="85248-172">Contient des informations d’accélération pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="85248-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="85248-173">Constantes</span><span class="sxs-lookup"><span data-stu-id="85248-173">Constants</span></span>



| <span data-ttu-id="85248-174">Rubrique</span><span class="sxs-lookup"><span data-stu-id="85248-174">Topic</span></span>                                                | <span data-ttu-id="85248-175">Contenu</span><span class="sxs-lookup"><span data-stu-id="85248-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="85248-176">Styles de contrôle up-up</span><span class="sxs-lookup"><span data-stu-id="85248-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="85248-177">Cette section répertorie les styles utilisés lors de la création de contrôles Up-Up.</span><span class="sxs-lookup"><span data-stu-id="85248-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 






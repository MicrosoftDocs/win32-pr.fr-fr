---
description: Winlogon et GINA doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des séquences de touches sécurisées et autoriser les activités de fermeture de session et d’arrêt.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Interaction entre Winlogon et GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035119"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="8dfcf-103">Interaction entre Winlogon et GINA</span><span class="sxs-lookup"><span data-stu-id="8dfcf-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="8dfcf-104">[*Winlogon*](../secgloss/w-gly.md) et [*Gina*](../secgloss/g-gly.md) doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des [*séquences de touches sécurisées*](../secgloss/s-gly.md) et autoriser les activités de fermeture de session et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="8dfcf-105">L’état de Winlogon détermine la fonction GINA appelée pour traiter tout événement SAS donné.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="8dfcf-106">Les communications se produisent dans l’ordre indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="8dfcf-107">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8dfcf-108">Événement</span><span class="sxs-lookup"><span data-stu-id="8dfcf-108">Event</span></span></th>
<th><span data-ttu-id="8dfcf-109">Description</span><span class="sxs-lookup"><span data-stu-id="8dfcf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8dfcf-110">Démarrage de station de travail</span><span class="sxs-lookup"><span data-stu-id="8dfcf-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="8dfcf-111">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de Gina pour notifier à Gina la version de Winlogon en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="8dfcf-112">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de la Gina pour fournir à la Gina les adresses des fonctions de prise en charge, un handle vers Winlogon et pour obtenir les informations de <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> de la Gina (à utiliser dans tous les appels futurs à Gina).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="8dfcf-113">Winlogon est dans l’état déconnecté.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8dfcf-114">Personne n’est connecté</span><span class="sxs-lookup"><span data-stu-id="8dfcf-114">No one is logged on</span></span></td>
<td><span data-ttu-id="8dfcf-115">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-116">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="8dfcf-117">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de la Gina, ce qui permet à Gina de traiter les informations d’identification et d’authentification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="8dfcf-118">Une fois l’ouverture de session réussie, Winlogon est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8dfcf-119">L’utilisateur a ouvert une session</span><span class="sxs-lookup"><span data-stu-id="8dfcf-119">The user is logged on</span></span></td>
<td><span data-ttu-id="8dfcf-120">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-121">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="8dfcf-122">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina, ce qui permet à Gina de présenter des options à l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8dfcf-123">L’utilisateur a ouvert une session et souhaite verrouiller l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="8dfcf-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="8dfcf-124">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-125">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8dfcf-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-126">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-127">GINA retourne WLX_SAS_ACTION_LOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="8dfcf-128">Winlogon est dans l’état verrouillé de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8dfcf-129">L’utilisateur a ouvert une session, la station de travail est verrouillée et l’utilisateur souhaite déverrouiller l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="8dfcf-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="8dfcf-130">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-131">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8dfcf-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-132">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-133">GINA retourne WLX_SAS_ACTION_UNLOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8dfcf-134">L’utilisateur a ouvert une session et le programme appelle la fonction <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8dfcf-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="8dfcf-135">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8dfcf-136">L’utilisateur a ouvert une session et souhaite se déconnecter à l’aide d’une signature d’accès partagé</span><span class="sxs-lookup"><span data-stu-id="8dfcf-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="8dfcf-137">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-138">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8dfcf-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-139">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-140">GINA retourne WLX_SAS_ACTION_LOGOFF.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="8dfcf-141">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8dfcf-142">L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide de <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8dfcf-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="8dfcf-143">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-144">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8dfcf-145">L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide d’une signature d’accès partagé</span><span class="sxs-lookup"><span data-stu-id="8dfcf-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="8dfcf-146">(Le GINA analyse les appareils pour les événements SAS).</span><span class="sxs-lookup"><span data-stu-id="8dfcf-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="8dfcf-147">GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8dfcf-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-148">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-149">GINA retourne WLX_SAS_ACTION_SHUTDOWN.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="8dfcf-150">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="8dfcf-151">Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 

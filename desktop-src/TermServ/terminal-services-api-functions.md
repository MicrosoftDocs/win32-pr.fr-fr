---
title: Services Bureau à distance les fonctions de l’API
description: Les fonctions suivantes sont utilisées avec Services Bureau à distance.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727980"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="558c2-103">Services Bureau à distance les fonctions de l’API</span><span class="sxs-lookup"><span data-stu-id="558c2-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="558c2-104">Les fonctions suivantes sont utilisées avec Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="558c2-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="558c2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="558c2-106">**ProcessIdToSessionId**</span><span class="sxs-lookup"><span data-stu-id="558c2-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="558c2-107">Récupère la session de Services Bureau à distance associée à un processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-108">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="558c2-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="558c2-109">Ouvre un handle vers le serveur de licences de Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-110">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="558c2-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="558c2-111">Ferme un handle ouvert sur un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-112">**TLSGetServerCertificate**</span><span class="sxs-lookup"><span data-stu-id="558c2-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="558c2-113">Retourne le certificat du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-114">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="558c2-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="558c2-115">Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="558c2-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-116">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="558c2-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="558c2-117">Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et met fin à l’énumération.</span><span class="sxs-lookup"><span data-stu-id="558c2-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-118">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="558c2-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="558c2-119">Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et retourne le prochain Pack de clés installé sur un serveur de licences bureau à distance qui correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="558c2-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-120">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="558c2-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="558c2-121">Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="558c2-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-122">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="558c2-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="558c2-123">Continue à partir d’un appel précédent à la fonction [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) et met fin à l’énumération.</span><span class="sxs-lookup"><span data-stu-id="558c2-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-124">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="558c2-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="558c2-125">Continue à partir d’un appel précédent à la fonction [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) et retourne la licence suivante qui est installée sur un serveur de licences bureau à distance qui correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="558c2-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-126">**VirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="558c2-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="558c2-127">Ferme l’extrémité client d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="558c2-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-128">**VirtualChannelEntry**</span><span class="sxs-lookup"><span data-stu-id="558c2-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="558c2-129">Point d’entrée défini par l’application pour la DLL côté client d’une application qui utilise Services Bureau à distance canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="558c2-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-130">**VirtualChannelInit**</span><span class="sxs-lookup"><span data-stu-id="558c2-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="558c2-131">Initialise l’accès d’une DLL client à Services Bureau à distance canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="558c2-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-132">*VirtualChannelInitEvent*</span><span class="sxs-lookup"><span data-stu-id="558c2-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="558c2-133">Fonction de rappel définie par l’application qui Services Bureau à distance appelle pour notifier la DLL client des événements de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="558c2-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-134">**VirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="558c2-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="558c2-135">Ouvre l’extrémité client d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="558c2-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-136">*VirtualChannelOpenEvent*</span><span class="sxs-lookup"><span data-stu-id="558c2-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="558c2-137">Fonction de rappel définie par l’application qui Services Bureau à distance appelle pour notifier la DLL client des événements pour un canal virtuel spécifique.</span><span class="sxs-lookup"><span data-stu-id="558c2-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-138">**VirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="558c2-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="558c2-139">Envoie des données de l’extrémité client d’un canal virtuel à une application partenaire côté serveur.</span><span class="sxs-lookup"><span data-stu-id="558c2-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-140">**WTSCloseServer**</span><span class="sxs-lookup"><span data-stu-id="558c2-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="558c2-141">Ferme un handle ouvert sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="558c2-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-142">**WTSConnectSession**</span><span class="sxs-lookup"><span data-stu-id="558c2-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="558c2-143">Connecte une session de Services Bureau à distance à une session existante sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="558c2-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-144">**WTSCreateListener**</span><span class="sxs-lookup"><span data-stu-id="558c2-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="558c2-145">Crée un écouteur de Services Bureau à distance ou configure un écouteur existant.</span><span class="sxs-lookup"><span data-stu-id="558c2-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-146">**WTSDisconnectSession**</span><span class="sxs-lookup"><span data-stu-id="558c2-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="558c2-147">Déconnecte l’utilisateur connecté de la session de Services Bureau à distance spécifiée sans fermer la session.</span><span class="sxs-lookup"><span data-stu-id="558c2-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-148">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="558c2-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="558c2-149">Active ou désactive les [sessions enfants](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="558c2-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="558c2-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="558c2-151">Énumère tous les écouteurs Services Bureau à distance sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-152">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="558c2-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="558c2-153">Récupère des informations sur les processus actifs sur un serveur hôte de session Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-154">**WTSEnumerateProcessesEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="558c2-155">Récupère des informations sur les processus actifs sur le serveur hôte de session Bureau à distance ou le serveur serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-156">**WTSEnumerateServers**</span><span class="sxs-lookup"><span data-stu-id="558c2-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="558c2-157">Retourne une liste de tous les serveurs hôtes de session Bureau à distance dans le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-158">**WTSEnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="558c2-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="558c2-159">Récupère une liste de sessions sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-160">**WTSEnumerateSessionsEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="558c2-161">Récupère une liste de sessions sur un serveur hôte de session Bureau à distance spécifié ou un serveur hôte de virtualisation des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-162">**WTSFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="558c2-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="558c2-163">Libère la mémoire allouée par une fonction Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-164">**WTSFreeMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="558c2-165">Libère de la mémoire qui contient les structures d’informations de [**\_ processus WTS \_ \_ ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) ou WTS, qui sont allouées par une fonction services Bureau à distance. [**\_ \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)</span><span class="sxs-lookup"><span data-stu-id="558c2-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-166">**WTSGetActiveConsoleSessionId**</span><span class="sxs-lookup"><span data-stu-id="558c2-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="558c2-167">Récupère l’identificateur de session de la session de console.</span><span class="sxs-lookup"><span data-stu-id="558c2-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-168">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="558c2-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="558c2-169">Récupère l’identificateur de session enfant, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="558c2-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-170">**WTSGetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="558c2-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="558c2-171">Récupère le descripteur de sécurité d’un écouteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-172">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="558c2-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="558c2-173">Détermine si les sessions enfants sont activées.</span><span class="sxs-lookup"><span data-stu-id="558c2-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-174">**WTSLogoffSession**</span><span class="sxs-lookup"><span data-stu-id="558c2-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="558c2-175">Déconnecte une session de Services Bureau à distance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="558c2-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-176">**WTSOpenServer**</span><span class="sxs-lookup"><span data-stu-id="558c2-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="558c2-177">Ouvre un handle vers le serveur hôte de session Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-178">**WTSOpenServerEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="558c2-179">Ouvre un handle vers le serveur hôte de session Bureau à distance spécifié ou le serveur hôte de virtualisation des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-180">**WTSQueryListenerConfig**</span><span class="sxs-lookup"><span data-stu-id="558c2-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="558c2-181">Récupère les informations de configuration d’un écouteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-182">**WTSQuerySessionInformation**</span><span class="sxs-lookup"><span data-stu-id="558c2-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="558c2-183">Récupère les informations de session pour la session spécifiée sur le serveur hôte de session Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-184">**WTSQueryUserConfig**</span><span class="sxs-lookup"><span data-stu-id="558c2-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="558c2-185">Récupère les informations de configuration pour l’utilisateur spécifié sur le contrôleur de domaine spécifié ou le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-186">**WTSQueryUserToken**</span><span class="sxs-lookup"><span data-stu-id="558c2-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="558c2-187">Obtient le jeton d’accès principal de l’utilisateur connecté spécifié par l’ID de session.</span><span class="sxs-lookup"><span data-stu-id="558c2-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-188">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="558c2-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="558c2-189">Inscrit la fenêtre spécifiée pour recevoir des notifications de modification de session.</span><span class="sxs-lookup"><span data-stu-id="558c2-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-190">**WTSRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="558c2-191">Inscrit la fenêtre spécifiée pour recevoir des notifications de modification de session.</span><span class="sxs-lookup"><span data-stu-id="558c2-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-192">**WTSSendMessage**</span><span class="sxs-lookup"><span data-stu-id="558c2-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="558c2-193">Affiche une boîte de message sur le Bureau du client d’une session de Services Bureau à distance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="558c2-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-194">**WTSSetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="558c2-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="558c2-195">Configure le descripteur de sécurité d’un écouteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-196">**WTSSetUserConfig**</span><span class="sxs-lookup"><span data-stu-id="558c2-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="558c2-197">Modifie les informations de configuration pour l’utilisateur spécifié sur le contrôleur de domaine spécifié ou le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-198">**WTSShutdownSystem**</span><span class="sxs-lookup"><span data-stu-id="558c2-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="558c2-199">Arrête (et éventuellement redémarre) le serveur hôte de session Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-200">**WTSStartRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="558c2-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="558c2-201">Démarre le contrôle à distance d’une autre session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="558c2-202">Vous devez appeler cette fonction à partir d’une session à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-203">**WTSStopRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="558c2-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="558c2-204">Arrête une session de contrôle à distance.</span><span class="sxs-lookup"><span data-stu-id="558c2-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-205">**WTSTerminateProcess**</span><span class="sxs-lookup"><span data-stu-id="558c2-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="558c2-206">Termine le processus spécifié sur le serveur hôte de session Bureau à distance spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="558c2-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="558c2-208">Annule l’inscription de la fenêtre spécifiée afin qu’elle ne reçoive plus de notifications de modification de session.</span><span class="sxs-lookup"><span data-stu-id="558c2-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-209">**WTSUnRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="558c2-210">Annule l’inscription de la fenêtre spécifiée afin qu’elle ne reçoive plus de notifications de modification de session.</span><span class="sxs-lookup"><span data-stu-id="558c2-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-211">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="558c2-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="558c2-212">Ferme un handle de canal virtuel ouvert.</span><span class="sxs-lookup"><span data-stu-id="558c2-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-213">**WTSVirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="558c2-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="558c2-214">Ouvre un handle vers l’extrémité serveur d’un canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-215">**WTSVirtualChannelOpenEx**</span><span class="sxs-lookup"><span data-stu-id="558c2-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="558c2-216">Crée un canal virtuel d’une manière similaire à [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span><span class="sxs-lookup"><span data-stu-id="558c2-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-217">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="558c2-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="558c2-218">Supprime toutes les données d’entrée mises en file d’attente envoyées du client au serveur sur un canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-219">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="558c2-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="558c2-220">Supprime toutes les données de sortie en file d’attente envoyées du serveur au client sur un canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-221">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="558c2-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="558c2-222">Retourne des informations sur un canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="558c2-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-223">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="558c2-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="558c2-224">Lit les données à partir de l’extrémité serveur d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="558c2-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-225">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="558c2-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="558c2-226">Écrit des données à l’extrémité serveur d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="558c2-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="558c2-227">**WTSWaitSystemEvent**</span><span class="sxs-lookup"><span data-stu-id="558c2-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="558c2-228">Attend un événement Services Bureau à distance avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="558c2-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 
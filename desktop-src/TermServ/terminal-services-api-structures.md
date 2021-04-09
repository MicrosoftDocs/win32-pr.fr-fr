---
title: Structures d’API Services Bureau à distance
description: Répertorie les structures utilisées avec l’API Services Bureau à distance.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101689"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="2ec02-103">Structures d’API Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="2ec02-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="2ec02-104">Les structures suivantes sont utilisées avec l’API Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ec02-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2ec02-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2ec02-106">**définition de canal \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="2ec02-107">Contient le nom et les options d’une Services Bureau à distance canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="2ec02-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-108">**\_points d’entrée du canal \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="2ec02-109">Contient des pointeurs vers les fonctions appelées par une DLL côté client pour accéder aux canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="2ec02-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-110">**\_ \_ en-tête de PDU de canal**</span><span class="sxs-lookup"><span data-stu-id="2ec02-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="2ec02-111">Contient des informations sur un bloc de données reçu par l’extrémité serveur d’un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="2ec02-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-112">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="2ec02-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="2ec02-113">Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.</span><span class="sxs-lookup"><span data-stu-id="2ec02-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-114">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="2ec02-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="2ec02-115">Contient des informations sur une licence de Services Bureau à distance spécifique.</span><span class="sxs-lookup"><span data-stu-id="2ec02-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-116">**WTSCLIENT**</span><span class="sxs-lookup"><span data-stu-id="2ec02-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="2ec02-117">Contient des informations sur un client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="2ec02-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-118">**WTSCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="2ec02-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="2ec02-119">Contient des informations sur une session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-120">**WTSINFO**</span><span class="sxs-lookup"><span data-stu-id="2ec02-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="2ec02-121">Contient des informations sur une session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-122">**WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="2ec02-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="2ec02-123">Contient une Union de [**\_ niveau WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) qui contient des informations étendues sur une session de services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-124">**WTSINFOEX \_ niveau1**</span><span class="sxs-lookup"><span data-stu-id="2ec02-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="2ec02-125">Contient des informations étendues sur une session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-126">**WTSLISTENERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="2ec02-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="2ec02-127">Contient des informations sur un écouteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-128">**\_adresse IP \_ WTSSBX**</span><span class="sxs-lookup"><span data-stu-id="2ec02-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="2ec02-129">Contient des informations sur l’adresse IP d’une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="2ec02-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-130">**informations de connexion à la \_ machine WTSSBX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="2ec02-131">Contient des informations sur un ordinateur qui accepte les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-132">**\_informations sur la machine WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="2ec02-133">Contient des informations sur un ordinateur et son état actuel.</span><span class="sxs-lookup"><span data-stu-id="2ec02-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-134">**\_informations sur la session WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="2ec02-135">Contient des informations sur les sessions disponibles pour Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2ec02-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-136">**\_notification WTSSESSION**</span><span class="sxs-lookup"><span data-stu-id="2ec02-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="2ec02-137">Fournit des informations sur la notification de modification de session.</span><span class="sxs-lookup"><span data-stu-id="2ec02-137">Provides information about the session change notification.</span></span> <span data-ttu-id="2ec02-138">Un service reçoit cette structure dans sa fonction [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) en réponse à un événement de changement de session.</span><span class="sxs-lookup"><span data-stu-id="2ec02-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-139">**WTSUSERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="2ec02-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="2ec02-140">Contient les informations de configuration d’un utilisateur sur un contrôleur de domaine ou un serveur d’hôte de session de Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2ec02-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-141">**\_adresse du client WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="2ec02-142">Contient l’adresse réseau du client d’une session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-143">**\_affichage du client WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="2ec02-144">Contient des informations sur l’affichage d’un client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="2ec02-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-145">**\_informations sur le processus WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="2ec02-146">Contient des informations sur un processus en cours d’exécution sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-147">**\_informations sur le processus WTS \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="2ec02-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="2ec02-148">Contient des informations étendues sur un processus en cours d’exécution sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="2ec02-149">[**\_informations sur le produit WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec02-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="2ec02-150">Détails de la licence de produit requise pour se connecter à un serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="2ec02-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-151">**\_informations sur le serveur WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="2ec02-152">Contient des informations sur un serveur de Services Bureau à distance spécifique.</span><span class="sxs-lookup"><span data-stu-id="2ec02-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-153">**\_adresse de session WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="2ec02-154">Contient l’adresse IP virtuelle assignée à une session.</span><span class="sxs-lookup"><span data-stu-id="2ec02-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-155">**\_informations sur la session WTS \_**</span><span class="sxs-lookup"><span data-stu-id="2ec02-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="2ec02-156">Contient des informations sur une session cliente sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ec02-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="2ec02-157">**\_Informations de session WTS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2ec02-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="2ec02-158">Contient des informations étendues sur une session cliente sur un serveur hôte de session Bureau à distance ou un serveur serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2ec02-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 
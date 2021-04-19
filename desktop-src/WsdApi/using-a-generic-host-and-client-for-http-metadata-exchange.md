---
description: Si le client et l’hôte ne peuvent pas échanger de métadonnées, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527775"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="a4491-103">Utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées HTTP</span><span class="sxs-lookup"><span data-stu-id="a4491-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="a4491-104">Si le client et l’hôte ne peuvent pas échanger de métadonnées, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="a4491-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="a4491-105">Si l’adresse de l’appareil ou les métadonnées de l’appareil n’apparaissent pas dans la sortie du client de débogage WSD, les adresses de transport ou l’environnement réseau fournis peuvent être à l’origine de l’échec.</span><span class="sxs-lookup"><span data-stu-id="a4491-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="a4491-106">Pour plus d’informations sur l’hôte et le client génériques, consultez [outils de débogage](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a4491-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="a4491-107">S’il a été vérifié qu’un hôte et un client génériques peuvent exécuter à la fois les WS-Discovery et l’échange de métadonnées HTTP, cette procédure de diagnostic peut être ignorée et la résolution des problèmes peut être poursuivie en suivant les procédures de la section utilisation de la [journalisation WinHTTP pour vérifier la récupération du trafic](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a4491-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="a4491-108">Si l’hôte ou le client est une application en cours d’exécution sur un PC, l’hôte ou le client générique doit être exécuté dans le même contexte de sécurité que l’hôte ou le client réel.</span><span class="sxs-lookup"><span data-stu-id="a4491-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="a4491-109">Par exemple, si l’hôte ou le client réel s’exécute en tant qu’administrateur, l’hôte ou le client générique doit s’exécuter en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a4491-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="a4491-110">En outre, si l’hôte ou le client est un appareil autonome, il doit être complètement remplacé par un PC exécutant un hôte ou un client générique dans un contexte de sécurité qui garantit un accès illimité au réseau (par exemple, l’exécution en tant qu’administrateur).</span><span class="sxs-lookup"><span data-stu-id="a4491-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="a4491-111">**Pour utiliser un hôte et un client génériques pour résoudre les problèmes liés à l’échange de métadonnées HTTP**</span><span class="sxs-lookup"><span data-stu-id="a4491-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="a4491-112">Ouvrir une fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a4491-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="a4491-113">Exécutez la commande suivante : **WSDDebug \_host.exe/mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="a4491-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="a4491-114">Une boîte de dialogue d' **alerte de sécurité Windows** peut s’afficher.</span><span class="sxs-lookup"><span data-stu-id="a4491-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="a4491-115">Dans ce cas, cliquez sur **débloquer** pour permettre l’exécution de l’hôte de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="a4491-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="a4491-116">Cette commande génère une sortie similaire à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="a4491-116">This command generates output similar to the following.</span></span> <span data-ttu-id="a4491-117">Prenez note de l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a4491-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="a4491-118">Exécutez la commande suivante : **WSDDebug \_client.exe les métadonnées/mode/Hello OFF/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="a4491-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="a4491-119">Remplacez *<id>* par l’ID d’appareil identifié à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a4491-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="a4491-120">Une boîte de dialogue d' **alerte de sécurité Windows** peut s’afficher.</span><span class="sxs-lookup"><span data-stu-id="a4491-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="a4491-121">Dans ce cas, cliquez sur **débloquer** pour permettre l’exécution du client de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="a4491-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="a4491-122">Le client de débogage WSD génère une sortie similaire à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="a4491-122">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="a4491-123">Le client de débogage WSD peut générer un grand nombre de sorties sur un réseau avec de nombreux appareils DPWS.</span><span class="sxs-lookup"><span data-stu-id="a4491-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="a4491-124">La sortie peut être redirigée vers un fichier pour faciliter l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a4491-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="a4491-125">Tapez **log tee** *<filename>* à l’invite du client de débogage WSD pour rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="a4491-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="a4491-126">La redirection de sortie peut être arrêtée en tapant **log tee Stop** à l’invite du client de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="a4491-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="a4491-127">Prenez note de l’adresse de référence du point de terminaison (EPR).</span><span class="sxs-lookup"><span data-stu-id="a4491-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="a4491-128">Cette adresse EPR doit correspondre à l’ID d’appareil identifié à l’étape 2 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a4491-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="a4491-129">Vérifiez également que le client de débogage WSD a complètement imprimé les métadonnées de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a4491-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="a4491-130">Les métadonnées de l’appareil commencent par `Metadata for host` et se terminent par `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="a4491-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="a4491-131">Si l’ID d’appareil et les métadonnées de l’appareil s’affichent correctement dans la sortie du client de débogage WSD, l’échec de l’application n’est probablement pas lié aux adresses de transport, au système d’exploitation ou à l’environnement réseau fournis.</span><span class="sxs-lookup"><span data-stu-id="a4491-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="a4491-132">Remplacez l’hôte et le client génériques par l’hôte et le client personnalisés, puis poursuivez le dépannage en suivant les procédures de la section utilisation de la [journalisation WinHTTP pour vérifier la récupération du trafic](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a4491-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="a4491-133">Si l’adresse de l’appareil et les métadonnées de l’appareil n’apparaissent pas dans la sortie du client de débogage WSD, l’échec peut avoir une ou plusieurs des causes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4491-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="a4491-134">L’adresse de transport publiée par l’hôte est incorrecte ou incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a4491-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="a4491-135">Le client de débogage WSD tente d’obtenir les métadonnées de l’appareil à partir de l’URL fournie dans l’élément **XAddrs** d’un message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="a4491-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="a4491-136">L’URL utilisée pour l’échange de métadonnées s’affiche dans la sortie du client de débogage WSD, préfixée par l’expression `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="a4491-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="a4491-137">L’exemple suivant montre le XAddrs utilisé pour l’échange de métadonnées dans la sortie du client de débogage WSD ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a4491-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="a4491-138">Si les XAddrs spécifiés ne sont pas conformes aux [règles de validation XAddr](xaddr-validation-rules.md), le client de débogage WSD ne peut pas récupérer les métadonnées de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a4491-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="a4491-139">L’application s’exécute dans un contexte de sécurité incorrect.</span><span class="sxs-lookup"><span data-stu-id="a4491-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="a4491-140">Vérifiez que l’application utilise les informations d’identification correctes et que le client et l’hôte disposent des autorisations suffisantes pour accéder au réseau.</span><span class="sxs-lookup"><span data-stu-id="a4491-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="a4491-141">La configuration du pare-feu est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a4491-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="a4491-142">Suivez les instructions de la [section inspection des paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md) pour vérifier que les paramètres du pare-feu Windows sont corrects et qu’aucune autre règle ne supprime les paquets.</span><span class="sxs-lookup"><span data-stu-id="a4491-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="a4491-143">Le client et l’hôte peuvent également être copiés sur un ordinateur « initial » (l’un avec une installation de système d’exploitation par défaut qui n’a jamais été jointe à un domaine) afin de tenter de reproduire l’échec.</span><span class="sxs-lookup"><span data-stu-id="a4491-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="a4491-144">Une stratégie IPSec bloque l’application.</span><span class="sxs-lookup"><span data-stu-id="a4491-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="a4491-145">Copiez le client et l’hôte sur un ordinateur qui n’est pas soumis aux stratégies IPSec et essayez de reproduire l’échec.</span><span class="sxs-lookup"><span data-stu-id="a4491-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4491-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4491-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4491-147">Procédures de diagnostic WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a4491-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="a4491-148">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a4491-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




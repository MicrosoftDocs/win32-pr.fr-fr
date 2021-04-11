---
title: Activation du suivi EAPHost
description: Peut aider les utilisateurs à trouver les causes racines des problèmes qui se produisent pendant le processus d’authentification EAP. Les informations de débogage peuvent inclure des appels d’API effectués, des appels de fonction internes effectués et des transitions d’État effectuées.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104032132"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="5eeaa-104">Activation du suivi EAPHost</span><span class="sxs-lookup"><span data-stu-id="5eeaa-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="5eeaa-105">Les journaux de suivi contenant des informations de débogage peuvent aider les utilisateurs à trouver les causes racines des problèmes qui se produisent pendant le processus d’authentification EAP.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="5eeaa-106">Les informations de débogage peuvent inclure des appels d’API effectués, des appels de fonction internes effectués et des transitions d’État effectuées.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="5eeaa-107">Le suivi peut être activé côté client et côté authentificateur.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="5eeaa-108">Le suivi peut également être activé pour les appels aux API du [service de routage et d’accès à distance (RRAS)](/windows/desktop/RRAS/routing-start-page) .</span><span class="sxs-lookup"><span data-stu-id="5eeaa-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="5eeaa-109">Pour plus d’informations, consultez [suivi sur le service Routage et accès distant](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="5eeaa-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="5eeaa-110">Les journaux de suivi sont disponibles en anglais uniquement.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="5eeaa-111">Quand le suivi EAPHost est activé, les informations de journalisation sont stockées dans un fichier. etl à un emplacement spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="5eeaa-112">Si des erreurs se produisent pendant l’authentification EAP, le suivi génère un fichier. etl qui peut être envoyé à Microsoft Developer Support pour l’analyse de la cause racine.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="5eeaa-113">Les partenaires qui ont accès aux partages de build, aux symboles et aux fichiers TraceFormat de Microsoft Windows peuvent convertir les fichiers. etl en fichier texte brut à l’aide de l’outil **Tracerpt** .</span><span class="sxs-lookup"><span data-stu-id="5eeaa-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="5eeaa-114">Les échecs du serveur de stratégie réseau (NPS) ne sont pas capturés dans les journaux EAPHost.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="5eeaa-115">Si vous essayez de résoudre un échec du serveur NPS, affichez le IASSAM. LOG et [IASNAP. Fichiers journaux](https://go.microsoft.com/fwlink/p/?linkid=84108) .</span><span class="sxs-lookup"><span data-stu-id="5eeaa-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="5eeaa-116">Suivi sur le client</span><span class="sxs-lookup"><span data-stu-id="5eeaa-116">Tracing on the Client</span></span>

<span data-ttu-id="5eeaa-117">Pour activer le suivi côté client :</span><span class="sxs-lookup"><span data-stu-id="5eeaa-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="5eeaa-118">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="5eeaa-119">Exécutez la commande suivante : **Logman** **Start trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="5eeaa-120">Reproduisez le scénario que vous souhaitez tracer.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="5eeaa-121">Exécutez la commande suivante : **Logman** **Stop** **EapHostPeer** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="5eeaa-122">Convertissez le fichier ETL en texte à l’aide de la commande suivante : **Tracerpt EapHostPeer. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="5eeaa-123">Si vous n’avez pas accès à l’outil tracerpt, évitez la dernière étape et envoyez le fichier. etl à Microsoft Developer Support.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="5eeaa-124">Suivi sur l’authentificateur</span><span class="sxs-lookup"><span data-stu-id="5eeaa-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="5eeaa-125">Pour activer le suivi côté authentificateur :</span><span class="sxs-lookup"><span data-stu-id="5eeaa-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="5eeaa-126">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="5eeaa-127">Exécutez la commande suivante : **Logman** **Start trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="5eeaa-128">Reproduisez le scénario que vous souhaitez tracer.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="5eeaa-129">Exécutez la commande suivante : **Logman** **Stop** **EapHostAuthr** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="5eeaa-130">Convertissez le fichier ETL en texte à l’aide de la commande suivante : **Tracerpt EapHostAuthr. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="5eeaa-131">Si vous n’avez pas accès à l’outil tracerpt, évitez la dernière étape et envoyez plutôt le fichier. etl à Microsoft Developer Support.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="5eeaa-132">Suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="5eeaa-132">Event tracing</span></span>

<span data-ttu-id="5eeaa-133">Dans Windows 7 et les versions ultérieures de Windows, EapHost fournit un suivi basé sur les événements sur l’authentificateur et l’homologue.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="5eeaa-134">L’avantage du suivi basé sur les événements est qu’aucun fichier de symboles n’est nécessaire pour afficher les messages de trace.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="5eeaa-135">Pour activer le suivi d’événements :</span><span class="sxs-lookup"><span data-stu-id="5eeaa-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="5eeaa-136">Ouvrez **Observateur**.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="5eeaa-137">Les messages EapHost critiques sont journalisés sous : « vues personnalisées \\ événements d’administration »</span><span class="sxs-lookup"><span data-stu-id="5eeaa-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="5eeaa-138">Les messages non critiques sont journalisés sous : «applications et services \\ Microsoft \\ Windows \\ EAPHost</span><span class="sxs-lookup"><span data-stu-id="5eeaa-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="5eeaa-139">Les messages d’événements de type « analyse » et « débogage » peuvent être affichés sous le même chemin d’accès en sélectionnant **afficher les journaux d’analyse et de débogage** dans le menu **affichage** de la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="5eeaa-140">Suivi sur le service Routage et accès distant</span><span class="sxs-lookup"><span data-stu-id="5eeaa-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="5eeaa-141">Pour activer le suivi RRAS :</span><span class="sxs-lookup"><span data-stu-id="5eeaa-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="5eeaa-142">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="5eeaa-143">Exécutez la commande suivante : **netsh** **RAS** **Set** **TR** **\* *_ _* fr**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="5eeaa-144">Ouvrir **\\ le suivi% systemroot%** pour afficher les traces RAS</span><span class="sxs-lookup"><span data-stu-id="5eeaa-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="5eeaa-145">Pour désactiver le suivi RRAS :</span><span class="sxs-lookup"><span data-stu-id="5eeaa-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="5eeaa-146">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="5eeaa-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="5eeaa-147">Exécutez la commande suivante : **netsh** **RAS** **Set** **TR** **\* *_ _* dis**</span><span class="sxs-lookup"><span data-stu-id="5eeaa-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="5eeaa-148">Pour plus d’informations, consultez [commandes netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="5eeaa-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eeaa-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eeaa-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eeaa-150">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="5eeaa-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="5eeaa-151">Service Routage et accès à distance</span><span class="sxs-lookup"><span data-stu-id="5eeaa-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 
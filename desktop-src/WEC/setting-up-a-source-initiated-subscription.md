---
title: Configuration d’un abonnement initié par la source
description: Les abonnements initiés par la source vous permettent de définir un abonnement sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements, puis plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/04/2020
ms.locfileid: "104381755"
---
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="c8754-103">Configuration d’un abonnement initié par la source</span><span class="sxs-lookup"><span data-stu-id="c8754-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="c8754-104">Les abonnements initiés par la source vous permettent de définir un abonnement sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements, puis plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="c8754-105">Cela diffère d’un abonnement initié par le collecteur, car dans le modèle d’abonnement initié par le collecteur, le collecteur d’événements doit définir toutes les sources d’événements dans l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="c8754-106">Lors de la configuration d’un abonnement initié par la source, déterminez si les ordinateurs source d’événements se trouvent dans le même domaine que l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="c8754-107">Les sections suivantes décrivent les étapes à suivre lorsque les sources d’événements se trouvent dans le même domaine ou non dans le même domaine que l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="c8754-108">Tout ordinateur d’un domaine, local ou distant, peut être un collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="c8754-109">Toutefois, lors du choix d’un collecteur d’événements, il est important de sélectionner un ordinateur proche de la topologie topologique où la majorité des événements seront générés.</span><span class="sxs-lookup"><span data-stu-id="c8754-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="c8754-110">L’envoi d’événements à un ordinateur situé à un emplacement réseau distant sur un réseau étendu peut réduire les performances globales et l’efficacité de la collecte d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="c8754-111">Configuration d’un abonnement initié par le code source dans lequel les sources d’événements se trouvent dans le même domaine que l’ordinateur du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="c8754-112">Les ordinateurs source d’événements et l’ordinateur du collecteur d’événements doivent être configurés pour configurer un abonnement initié par la source.</span><span class="sxs-lookup"><span data-stu-id="c8754-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="c8754-113">Ces instructions partent du principe que vous disposez d’un accès administrateur au contrôleur de domaine Windows Server desservant le domaine dans lequel l’ordinateur ou les ordinateurs distants sont configurés pour collecter des événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="c8754-114">Configuration de l’ordinateur source de l’événement</span><span class="sxs-lookup"><span data-stu-id="c8754-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="c8754-115">Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour configurer Windows Remote Management :</span><span class="sxs-lookup"><span data-stu-id="c8754-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="c8754-116">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="c8754-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="c8754-117">Démarrez la stratégie de groupe en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="c8754-118">**% SYSTEMROOT% \\ system32 \\ gpedit. msc**</span><span class="sxs-lookup"><span data-stu-id="c8754-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="c8754-119">Sous le nœud **configuration** de l’ordinateur, développez le nœud **modèles d’administration** , développez le nœud **composants Windows** , puis sélectionnez le nœud **transfert d’événements** .</span><span class="sxs-lookup"><span data-stu-id="c8754-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="c8754-120">Cliquez avec le bouton droit sur le paramètre **SubscriptionManager** , puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c8754-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="c8754-121">Activez le paramètre **SubscriptionManager** , puis cliquez sur le bouton **Afficher** pour ajouter une adresse de serveur au paramètre.</span><span class="sxs-lookup"><span data-stu-id="c8754-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="c8754-122">Ajoutez au moins un paramètre qui spécifie l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="c8754-123">La fenêtre **Propriétés de SubscriptionManager** contient un onglet **expliquer** qui décrit la syntaxe du paramètre.</span><span class="sxs-lookup"><span data-stu-id="c8754-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="c8754-124">Une fois le paramètre **SubscriptionManager** ajouté, exécutez la commande suivante pour vous assurer que la stratégie est appliquée :</span><span class="sxs-lookup"><span data-stu-id="c8754-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="c8754-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="c8754-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="c8754-126">Configuration de l’ordinateur du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="c8754-127">Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour configurer Windows Remote Management :</span><span class="sxs-lookup"><span data-stu-id="c8754-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="c8754-128">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="c8754-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="c8754-129">Exécutez la commande suivante pour configurer le service collecteur d’événements :</span><span class="sxs-lookup"><span data-stu-id="c8754-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="c8754-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="c8754-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="c8754-131">Créez un abonnement initié par la source.</span><span class="sxs-lookup"><span data-stu-id="c8754-131">Create a source initiated subscription.</span></span> <span data-ttu-id="c8754-132">Vous pouvez effectuer cette opération par programme, à l’aide de l’observateur d’événements ou à l’aide de [**Wecutil.exe**](wecutil.md).</span><span class="sxs-lookup"><span data-stu-id="c8754-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="c8754-133">Pour plus d’informations sur la création de l’abonnement par programme, consultez l’exemple de code relatif à la [création d’un abonnement initié](creating-a-source-initiated-subscription.md)par la source.</span><span class="sxs-lookup"><span data-stu-id="c8754-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="c8754-134">Si vous utilisez Wecutil.exe, vous devez créer un fichier XML d’abonnement aux événements et utiliser la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="c8754-135"> *configurationFile.xml* de la ressource.</span><span class="sxs-lookup"><span data-stu-id="c8754-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="c8754-136">Le code XML suivant est un exemple du contenu d’un fichier de configuration d’abonnement qui crée un abonnement initié par la source pour transférer des événements du journal des événements d’application d’un ordinateur distant vers le journal ForwardedEvents sur l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > <span data-ttu-id="c8754-137">Lors de la création d’un abonnement initié par la source, si AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList et DeniedSubjectList sont tous vides, "O :NSG : NSD : (A ;; GA ;;;D C) (A ;; GA ;;; NS)» sera utilisé comme descripteur de sécurité par défaut pour AllowedSourceDomainComputers.</span><span class="sxs-lookup"><span data-stu-id="c8754-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="c8754-138">Le descripteur par défaut accorde aux membres du groupe de domaine ordinateurs du domaine, ainsi qu’au groupe de service réseau local (pour le redirecteur local), la possibilité de déclencher des événements pour cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8754-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="c8754-139">Pour valider le bon fonctionnement de l’abonnement</span><span class="sxs-lookup"><span data-stu-id="c8754-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="c8754-140">Sur l’ordinateur du collecteur d’événements, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8754-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="c8754-141">Exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges sur le contrôleur de domaine Windows Server pour récupérer l’état d’exécution de l’abonnement :</span><span class="sxs-lookup"><span data-stu-id="c8754-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="c8754-142">**wecutil gr** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="c8754-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="c8754-143">Vérifiez que la source de l’événement est connectée.</span><span class="sxs-lookup"><span data-stu-id="c8754-143">Verify that the event source has connected.</span></span> <span data-ttu-id="c8754-144">Vous devrez peut-être attendre que l’intervalle d’actualisation spécifié dans la stratégie soit dépassé après avoir créé l’abonnement pour la source d’événements à connecter.</span><span class="sxs-lookup"><span data-stu-id="c8754-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="c8754-145">Exécutez la commande suivante pour récupérer les informations d’abonnement :</span><span class="sxs-lookup"><span data-stu-id="c8754-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="c8754-146">**wecutil GS** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="c8754-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="c8754-147">Obtient la valeur DeliveryMaxItems à partir des informations d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8754-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="c8754-148">Sur l’ordinateur source de l’événement, déclenchez les événements qui correspondent à la requête de l’abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="c8754-149">Le nombre d’événements DeliveryMaxItems doit être déclenché pour que les événements soient transférés.</span><span class="sxs-lookup"><span data-stu-id="c8754-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="c8754-150">Sur l’ordinateur du collecteur d’événements, vérifiez que les événements ont été transférés dans le journal ForwardedEvents ou dans le journal spécifié dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8754-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="c8754-151">Transfert du journal de sécurité</span><span class="sxs-lookup"><span data-stu-id="c8754-151">Forwarding the security log</span></span>

<span data-ttu-id="c8754-152">Pour pouvoir transférer le journal de sécurité, vous devez ajouter le compte SERVICE réseau au groupe lecteurs EventLog.</span><span class="sxs-lookup"><span data-stu-id="c8754-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="c8754-153">Configuration d’un abonnement initié par la source lorsque les sources d’événements ne se trouvent pas dans le même domaine que l’ordinateur du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="c8754-154">Ces instructions partent du principe que vous disposez d’un accès administrateur à un contrôleur de domaine Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c8754-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="c8754-155">Dans ce cas, étant donné que l’ordinateur ou les ordinateurs collecteurs d’événements distants ne sont pas dans le domaine pris en charge par le contrôleur de domaine, il est essentiel de démarrer un client individuel en définissant Windows Remote Management sur « automatique » à l’aide de services (services. msc).</span><span class="sxs-lookup"><span data-stu-id="c8754-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="c8754-156">Vous pouvez également exécuter « WinRM quickconfig » sur chaque client distant.</span><span class="sxs-lookup"><span data-stu-id="c8754-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="c8754-157">Les conditions préalables suivantes doivent être remplies pour que l’abonnement soit créé.</span><span class="sxs-lookup"><span data-stu-id="c8754-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="c8754-158">Sur l’ordinateur du collecteur d’événements, exécutez les commandes suivantes à partir d’une invite de commandes avec élévation de privilèges pour configurer Windows Remote Management et le service collecteur d’événements :</span><span class="sxs-lookup"><span data-stu-id="c8754-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="c8754-159">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="c8754-159">**winrm qc -q**</span></span>

    <span data-ttu-id="c8754-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="c8754-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="c8754-161">L’ordinateur collecteur doit avoir un certificat d’authentification serveur (certificat avec un rôle d’authentification serveur) dans un magasin de certificats de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c8754-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="c8754-162">Sur l’ordinateur source de l’événement, exécutez la commande suivante pour configurer Windows Remote Management :</span><span class="sxs-lookup"><span data-stu-id="c8754-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="c8754-163">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="c8754-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="c8754-164">L’ordinateur source doit avoir un certificat d’authentification client (certificat avec un rôle d’authentification du client) dans un magasin de certificats de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c8754-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="c8754-165">Le port 5986 est ouvert sur l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="c8754-166">Pour ouvrir ce port, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-166">To open this port, run the command:</span></span>

    <span data-ttu-id="c8754-167">**netsh firewall Add ouverture TCP 5986 "gestion à distance de WinRM HTTPs"**</span><span class="sxs-lookup"><span data-stu-id="c8754-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="c8754-168">Certificats requis</span><span class="sxs-lookup"><span data-stu-id="c8754-168">Certificates requirements</span></span>

- <span data-ttu-id="c8754-169">Un certificat d’authentification serveur doit être installé sur l’ordinateur du collecteur d’événements dans le magasin personnel de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c8754-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="c8754-170">L’objet de ce certificat doit correspondre au nom de domaine complet du collecteur.</span><span class="sxs-lookup"><span data-stu-id="c8754-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="c8754-171">Un certificat d’authentification client doit être installé sur les ordinateurs source d’événements dans le magasin personnel de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c8754-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="c8754-172">L’objet de ce certificat doit correspondre au nom de domaine complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c8754-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="c8754-173">Si le certificat client a été émis par une autorité de certification différente de celle du collecteur d’événements, ces certificats racine et intermédiaires doivent également être installés sur le collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="c8754-174">Si le certificat client a été émis par une autorité de certification intermédiaire et que le collecteur exécute Windows 2012 ou une version ultérieure, vous devrez configurer la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="c8754-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="c8754-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="c8754-176">Vérifiez que le serveur et le client sont correctement en mesure de vérifier l’état de révocation sur tous les certificats.</span><span class="sxs-lookup"><span data-stu-id="c8754-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="c8754-177">L’utilisation de la commande **certutil** peut aider à résoudre les erreurs éventuelles.</span><span class="sxs-lookup"><span data-stu-id="c8754-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="c8754-178">Pour plus d’informations, consultez cet article : https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="c8754-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="c8754-179">Configurer l’écouteur sur le collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="c8754-180">Définissez l’authentification par certificat à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="c8754-181">**winrm set winrm/config/service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="c8754-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="c8754-182">Un écouteur HTTPs WinRM avec le certificat d’authentification serveur Print Thumb doit exister sur l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="c8754-183">Vous pouvez le vérifier à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="c8754-184">**WinRM e winrm/config/Listener**</span><span class="sxs-lookup"><span data-stu-id="c8754-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="c8754-185">Si vous ne voyez pas l’écouteur HTTPs, ou si le curseur de l’écouteur HTTPs n’est pas le même que le curseur d’impression du certificat d’authentification serveur sur l’ordinateur collecteur, vous pouvez supprimer cet écouteur et en créer un nouveau avec l’impression appropriée.</span><span class="sxs-lookup"><span data-stu-id="c8754-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="c8754-186">Pour supprimer l’écouteur https, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="c8754-187">**WinRM supprimer winrm/config/Listener ? Adresse = \* + transport = HTTPs**</span><span class="sxs-lookup"><span data-stu-id="c8754-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="c8754-188">Pour créer un nouvel écouteur, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="c8754-189">**WinRM créer winrm/config/Listener ? Adresse =&#42;+ transport = HTTPS @ {hostname = "** &lt; _nom de domaine complet du collecteur_ &gt; **"; CertificateThumbprint = "** &lt; _impression au pouce du certificat d’authentification serveur_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="c8754-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="c8754-190">Configurer le mappage de certificat sur le collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="c8754-191">Créez un utilisateur local et ajoutez-le au groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="c8754-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="c8754-192">Créez le mappage de certificat à l’aide d’un certificat qui est présent dans les « autorités de certification racines de confiance » de l’ordinateur ou « autorités de certification intermédiaires ».</span><span class="sxs-lookup"><span data-stu-id="c8754-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="c8754-193">Il s’agit du certificat de l’autorité de certification racine ou intermédiaire qui a émis les certificats installés sur les ordinateurs de la source *d’événements (pour éviter toute confusion, il s’agit de l’autorité de certification située immédiatement au-dessus du certificat dans la chaîne de certificats)*:</span><span class="sxs-lookup"><span data-stu-id="c8754-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="c8754-194">**WinRM créer winrm/config/service/certmapping ?** = &lt; _Empreinte numérique du certificat de l’autorité de certification émettrice_ &gt; **+ Subject =&#42;+ URI =&#42; @ {nom d’utilisateur = "** &lt; _username_ &gt; **"; Password = "** &lt; _mot_de_passe_ &gt; **"}-distant : localhost**</span><span class="sxs-lookup"><span data-stu-id="c8754-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="c8754-195">À partir d’un client, testez l’écouteur et le mappage de certificat à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="c8754-196">**WinRM g winrm/config-r :https://** &lt; _Nom de domaine complet_ &gt; du collecteur d’événements **: 5986-a :Certificate-Certificat :»** &lt; _Empreinte numérique du certificat_ &gt; d’authentification client **"**</span><span class="sxs-lookup"><span data-stu-id="c8754-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="c8754-197">Elle doit retourner la configuration WinRM du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="c8754-198">**Ne** dépassez pas cette étape si la configuration n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="c8754-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="c8754-199">**Que se passe-t-il à cette étape ?**</span><span class="sxs-lookup"><span data-stu-id="c8754-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="c8754-200">Le client se connecte au collecteur d’événements et envoie le certificat spécifié</span><span class="sxs-lookup"><span data-stu-id="c8754-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="c8754-201">Le collecteur d’événements recherche l’autorité de certification émettrice et vérifie si le est un mappage de certificat correspondant</span><span class="sxs-lookup"><span data-stu-id="c8754-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="c8754-202">Le collecteur d’événements valide l’état de la chaîne de certificats du client et des révocations</span><span class="sxs-lookup"><span data-stu-id="c8754-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="c8754-203">Si les étapes ci-dessus réussissent, l’authentification est terminée.</span><span class="sxs-lookup"><span data-stu-id="c8754-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="c8754-204">Vous pouvez obtenir une erreur d’accès refusé lors de la méthode d’authentification, ce qui peut être trompeur.</span><span class="sxs-lookup"><span data-stu-id="c8754-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="c8754-205">Pour résoudre les problèmes, consultez le journal CAPI sur le collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="c8754-206">Répertoriez les entrées certmapping configurées à l’aide de la commande : **WinRM enum winrm/config/service/certmapping**</span><span class="sxs-lookup"><span data-stu-id="c8754-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="c8754-207">Configuration de l’ordinateur source d’événements</span><span class="sxs-lookup"><span data-stu-id="c8754-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="c8754-208">Ouverture de session avec un compte d’administrateur et ouverture de l’éditeur de stratégie de groupe local (gpedit. msc)</span><span class="sxs-lookup"><span data-stu-id="c8754-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="c8754-209">Accédez à l’ordinateur local Local\configuration \ modèles d’administration\Composants Components\Event de transfert.</span><span class="sxs-lookup"><span data-stu-id="c8754-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="c8754-210">Ouvrez la stratégie « configurer l’adresse du serveur, l’intervalle d’actualisation et l’autorité de certification de l’émetteur d’un gestionnaire d’abonnements cible ».</span><span class="sxs-lookup"><span data-stu-id="c8754-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="c8754-211">Activez la stratégie et cliquez sur le SubscriptionManagers « afficher... » bouton.</span><span class="sxs-lookup"><span data-stu-id="c8754-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="c8754-212">Dans la fenêtre SubscriptionManagers, entrez la chaîne suivante :</span><span class="sxs-lookup"><span data-stu-id="c8754-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="c8754-213">**Serveur = https://** &lt; _Nom de domaine complet du serveur_ &gt; collecteur d’événements **: 5986/WSMan/SubscriptionManager/WEC, Refresh =** &lt; _Intervalle d’actualisation en secondes_ &gt; **, IssuerCA =** &lt; _Empreinte numérique du certificat de l’autorité de certification émettrice_&gt;</span><span class="sxs-lookup"><span data-stu-id="c8754-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="c8754-214">Exécutez la ligne de commande suivante pour actualiser les paramètres de stratégie de groupe locaux : gpupdate/force</span><span class="sxs-lookup"><span data-stu-id="c8754-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="c8754-215">Ces étapes doivent générer l’événement 104 dans votre ordinateur source observateur d’événements journal des applications et des services avec le message suivant :</span><span class="sxs-lookup"><span data-stu-id="c8754-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="c8754-216">« Le redirecteur s’est correctement connecté au gestionnaire d’abonnement au &lt; nom de domaine complet de l’adresse &gt; , suivi de l’événement 100 avec le message suivant : «l’abonnement &lt; sub_name &gt; est correctement créé ».</span><span class="sxs-lookup"><span data-stu-id="c8754-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="c8754-217">Dans le collecteur d’événements, l’état d’exécution de l’abonnement affiche maintenant 1 ordinateur actif.</span><span class="sxs-lookup"><span data-stu-id="c8754-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="c8754-218">Ouvrez le journal ForwardedEvents sur le collecteur d’événements et vérifiez si les événements sont transférés à partir des ordinateurs sources.</span><span class="sxs-lookup"><span data-stu-id="c8754-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="c8754-219">Accorder l’autorisation sur la clé privée du certificat client sur la source de l’événement</span><span class="sxs-lookup"><span data-stu-id="c8754-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="c8754-220">Ouvrez la console de gestion des certificats pour l’ordinateur local sur l’ordinateur source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="c8754-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="c8754-221">Cliquez avec le bouton droit sur le certificat client, puis sur gérer les clés privées.</span><span class="sxs-lookup"><span data-stu-id="c8754-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="c8754-222">Accordez une autorisation de lecture à l’utilisateur du SERVICE réseau.</span><span class="sxs-lookup"><span data-stu-id="c8754-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="c8754-223">Configuration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="c8754-223">Event subscription configuration</span></span>

1. <span data-ttu-id="c8754-224">Ouvrez observateur d’événements dans le collecteur d’événements et accédez au nœud abonnements.</span><span class="sxs-lookup"><span data-stu-id="c8754-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="c8754-225">Cliquez avec le bouton droit sur abonnements, puis choisissez « créer un abonnement... ».</span><span class="sxs-lookup"><span data-stu-id="c8754-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="c8754-226">Donnez un nom et une description facultative pour le nouvel abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8754-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="c8754-227">Sélectionnez l’option « initiée par l’ordinateur source », puis cliquez sur « Sélectionner des groupes d’ordinateurs... ».</span><span class="sxs-lookup"><span data-stu-id="c8754-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="c8754-228">Dans groupes d’ordinateurs, cliquez sur « Ajouter des ordinateurs non-domaines... ».</span><span class="sxs-lookup"><span data-stu-id="c8754-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="c8754-229">et tapez le nom d’hôte de la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="c8754-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="c8754-230">Cliquez sur « Ajouter des certificats... »</span><span class="sxs-lookup"><span data-stu-id="c8754-230">Click “Add Certificates…”</span></span> <span data-ttu-id="c8754-231">et ajoutez le certificat de l’autorité de certification qui émet les certificats clients.</span><span class="sxs-lookup"><span data-stu-id="c8754-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="c8754-232">Vous pouvez cliquer sur Afficher le certificat pour valider le certificat.</span><span class="sxs-lookup"><span data-stu-id="c8754-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="c8754-233">Dans autorités de certification, cliquez sur OK pour ajouter le certificat.</span><span class="sxs-lookup"><span data-stu-id="c8754-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="c8754-234">Lorsque vous avez terminé d’ajouter des ordinateurs, cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="c8754-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="c8754-235">Dans les propriétés de l’abonnement, cliquez dans sélectionner des événements...</span><span class="sxs-lookup"><span data-stu-id="c8754-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="c8754-236">Configurez le filtre de requête des événements en spécifiant le ou les niveaux d’événement, les journaux des événements ou la ou les sources d’événements, les ID d’événement et toutes les autres options de filtrage.</span><span class="sxs-lookup"><span data-stu-id="c8754-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="c8754-237">Dans les propriétés de l’abonnement, cliquez sur avancé...</span><span class="sxs-lookup"><span data-stu-id="c8754-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="c8754-238">Choisissez l’une des options d’optimisation pour la remise d’événements de l’événement source vers le collecteur d’événements, ou laissez la valeur par défaut normal :</span><span class="sxs-lookup"><span data-stu-id="c8754-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="c8754-239">**Réduire la bande passante**: les événements seront remis moins de fréquence pour économiser la bande passante.</span><span class="sxs-lookup"><span data-stu-id="c8754-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="c8754-240">**Réduire la latence**: les événements sont remis dès qu’ils se produisent pour réduire la latence des événements.</span><span class="sxs-lookup"><span data-stu-id="c8754-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="c8754-241">Remplacez le protocole par HTTPs et cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="c8754-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="c8754-242">Cliquez sur OK pour créer le nouvel abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8754-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="c8754-243">Vérifiez l’état d’exécution de l’abonnement en cliquant avec le bouton droit et en sélectionnant « état de l’exécution ».</span><span class="sxs-lookup"><span data-stu-id="c8754-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>

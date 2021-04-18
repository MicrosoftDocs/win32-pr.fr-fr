---
description: Si l’hôte et le client génériques peuvent s’afficher mutuellement sur le réseau, mais que l’hôte et le client réels ne le sont pas, il est probable que le problème se trouve dans les messages envoyés entre les points de terminaison sur le réseau.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519722"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="4e359-103">Utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="4e359-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="4e359-104">Si l’hôte et le client génériques peuvent s’afficher mutuellement sur le réseau, mais que l’hôte et le client réels ne le sont pas, il est probable que le problème se trouve dans les messages envoyés entre les points de terminaison sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4e359-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="4e359-105">Pour plus d’informations sur l’hôte et le client génériques, consultez [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4e359-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="4e359-106">Étant donné que les traces de réseau complètes peuvent être difficiles à collecter, à filtrer et à lire, l’outil client de débogage WSD peut être utilisé pour imprimer les côtés de la multidiffusion des messages WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="4e359-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="4e359-107">Le client de débogage WSD en mode multidiffusion ne peut inspecter que la moitié des messages, puisque le client ne peut pas imprimer les messages de monodiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="4e359-108">Si le trafic monodiffusion est digne d’intérêt, passez directement à l' [inspection des suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4e359-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="4e359-109">Cette procédure présente une méthode qui affiche tout le trafic de multidiffusion sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4e359-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="4e359-110">Pour afficher uniquement le trafic de multidiffusion à destination et en provenance de l’appareil, consultez la section [filtrage des résultats du client de débogage WSD](#filtering-wsd-debug-client-results) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4e359-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="4e359-111">**Pour utiliser le client de débogage WSD afin de vérifier le trafic de multidiffusion**</span><span class="sxs-lookup"><span data-stu-id="4e359-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="4e359-112">Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).</span><span class="sxs-lookup"><span data-stu-id="4e359-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4e359-113">Ouvrez une invite de commandes et exécutez la commande suivante : **WSDDebug \_client.exe la multidiffusion/mode**</span><span class="sxs-lookup"><span data-stu-id="4e359-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="4e359-114">Reproduisez l’erreur en démarrant l’hôte et le client ou en appuyant sur F5 dans l’Explorateur réseau.</span><span class="sxs-lookup"><span data-stu-id="4e359-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="4e359-115">Vérifiez que les messages sont en cours de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="4e359-116">Si les messages requis s’affichent dans la sortie du client de débogage WSD, l’échec de l’application peut être dans le contenu du message de multidiffusion, ou dans l’existence ou le contenu des messages de réponse de monodiffusion correspondants.</span><span class="sxs-lookup"><span data-stu-id="4e359-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="4e359-117">Poursuivez la résolution des problèmes en suivant les instructions fournies dans [inspection des suivis réseau pour UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="4e359-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="4e359-118">Si les messages requis s’affichent dans la sortie du client de débogage WSD, il est probable que la source du problème de l’application a été identifiée.</span><span class="sxs-lookup"><span data-stu-id="4e359-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="4e359-119">Il est probable que le trafic de multidiffusion n’est pas transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4e359-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="4e359-120">Cet échec peut se produire lorsque l’application n’énumère pas correctement les adaptateurs de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="4e359-121">Les applications doivent envoyer explicitement le trafic de multidiffusion sur toutes les interfaces réseau ; dans le cas contraire, les paquets ne peuvent pas être générés pour l’interface de bouclage ou pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="4e359-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="4e359-122">Pour vérifier que les paquets ne s’affichent pas sur le réseau, suivez les instructions de la procédure d' [inspection des suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md) et recherchez la preuve de l’absence de messages de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="4e359-123">Vérification de la multidiffusion des messages</span><span class="sxs-lookup"><span data-stu-id="4e359-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="4e359-124">Vérifiez toujours que les messages de [sondage](probe-message.md) sont en cours de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="4e359-125">Si vous le souhaitez, vérifiez que les messages de [salutation](hello-message.md) et de [résolution](resolve-message.md) sont en cours de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4e359-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="4e359-126">Notez que toutes les applications n’utilisent pas les messages de résolution.</span><span class="sxs-lookup"><span data-stu-id="4e359-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="4e359-127">Pour plus d’informations sur les modèles de message utilisés par les clients et les hôtes, consultez [modèles de message d’échange de métadonnées](discovery-and-metadata-exchange-message-patterns.md) et de découverte et [prise en main avec résolution des problèmes wsdapi](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="4e359-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="4e359-128">Les messages doivent être déclenchés pour pouvoir être envoyés comme décrit à l’étape 3 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4e359-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="4e359-129">Le client de débogage WSD affiche le message SOAP brut comme sortie.</span><span class="sxs-lookup"><span data-stu-id="4e359-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="4e359-130">Étant donné que tous les messages imprimés par le client de débogage WSD en mode de multidiffusion sont reçus sur un socket de multidiffusion, l’adresse de destination du message n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="4e359-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="4e359-131">L’exemple suivant de sortie du client de débogage WSD affiche un message de sondage.</span><span class="sxs-lookup"><span data-stu-id="4e359-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="4e359-132">L’élément <wsa : action> identifie le message en tant que message de sondage.</span><span class="sxs-lookup"><span data-stu-id="4e359-132">The <wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="4e359-133">Examinez le champ <wsa : action> pour vérifier que le message reçu était un message de sondage.</span><span class="sxs-lookup"><span data-stu-id="4e359-133">Inspect the <wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="4e359-134">L’exemple suivant de sortie du client de débogage WSD affiche un message de salutation.</span><span class="sxs-lookup"><span data-stu-id="4e359-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="4e359-135">L’élément <wsa : action> identifie le message en tant que message de salutation.</span><span class="sxs-lookup"><span data-stu-id="4e359-135">The <wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="4e359-136">Filtrage des résultats du client de débogage WSD</span><span class="sxs-lookup"><span data-stu-id="4e359-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="4e359-137">Le filtrage des résultats du client de débogage WSD peut aider à identifier le trafic d’incidents impliquant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e359-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="4e359-138">Le filtrage est uniquement nécessaire sur les réseaux bruyants.</span><span class="sxs-lookup"><span data-stu-id="4e359-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="4e359-139">Il existe deux façons de filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="4e359-139">There are two ways to filter results.</span></span> <span data-ttu-id="4e359-140">Les adresses IP à filtrer peuvent être identifiées explicitement lors du démarrage du client de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="4e359-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="4e359-141">Les adresses IP peuvent également être spécifiées après le démarrage du client.</span><span class="sxs-lookup"><span data-stu-id="4e359-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="4e359-142">Cette section décrit les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e359-142">This section describes both methods.</span></span>

<span data-ttu-id="4e359-143">**Pour spécifier des adresses IP à filtrer au démarrage du client de débogage WSD**</span><span class="sxs-lookup"><span data-stu-id="4e359-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="4e359-144">Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).</span><span class="sxs-lookup"><span data-stu-id="4e359-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4e359-145">Collectez la ou les adresses IP de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e359-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="4e359-146">Si l’appareil a plusieurs adresses (par exemple, il a à la fois des adresses IPv4 et IPv6), toutes les adresses doivent être collectées.</span><span class="sxs-lookup"><span data-stu-id="4e359-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="4e359-147">Ouvrez une invite de commandes et exécutez la commande suivante : \**WSDDebug \_client.exe/mode multicast/IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="4e359-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="4e359-148">*<device IP>* est une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="4e359-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="4e359-149">La liste suivante présente quelques exemples de formats pour cette adresse IP.</span><span class="sxs-lookup"><span data-stu-id="4e359-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="4e359-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="4e359-150">192.168.0.1</span></span>
-   <span data-ttu-id="4e359-151">::1</span><span class="sxs-lookup"><span data-stu-id="4e359-151">::1</span></span>
-   <span data-ttu-id="4e359-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4e359-152">mydevice.contoso.com</span></span>

<span data-ttu-id="4e359-153">Le client de débogage WSD résout automatiquement les noms d’hôte fournis à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="4e359-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="4e359-154">**Pour filtrer les résultats après le démarrage du client de débogage WSD**</span><span class="sxs-lookup"><span data-stu-id="4e359-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="4e359-155">Configurez l’hôte et le client pour qu’ils s’exécutent sur le réseau (autrement dit, assurez-vous que l’hôte et le client fonctionnent sur des ordinateurs différents).</span><span class="sxs-lookup"><span data-stu-id="4e359-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="4e359-156">Collectez la ou les adresses IP de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e359-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="4e359-157">Si l’appareil a plusieurs adresses (par exemple, il a à la fois des adresses IPv4 et IPv6), toutes les adresses doivent être collectées.</span><span class="sxs-lookup"><span data-stu-id="4e359-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="4e359-158">Ouvrez une invite de commandes et exécutez la commande suivante : **WSDDebug \_client.exe la multidiffusion/mode**</span><span class="sxs-lookup"><span data-stu-id="4e359-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="4e359-159">À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : \**Ajout d’adresses IP\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="4e359-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="4e359-160">Répétez l’étape 4 jusqu’à ce que toutes les adresses IP d’appareil aient été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="4e359-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="4e359-161">La procédure suivante suppose que le client de débogage WSD a été démarré et que le filtrage par adresse IP se produit.</span><span class="sxs-lookup"><span data-stu-id="4e359-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="4e359-162">**Pour vérifier que les adresses IP correctes sont filtrées**</span><span class="sxs-lookup"><span data-stu-id="4e359-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="4e359-163">À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : **Print IP**</span><span class="sxs-lookup"><span data-stu-id="4e359-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="4e359-164">La liste des adresses IP filtrées s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4e359-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="4e359-165">La procédure suivante suppose que le client de débogage WSD a été démarré et que le filtrage par adresse IP se produit.</span><span class="sxs-lookup"><span data-stu-id="4e359-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="4e359-166">**Pour désactiver le filtrage**</span><span class="sxs-lookup"><span data-stu-id="4e359-166">**To disable filtering**</span></span>

-   <span data-ttu-id="4e359-167">À l’invite de commandes du client de débogage WSD, exécutez la commande suivante : **IP Clear**</span><span class="sxs-lookup"><span data-stu-id="4e359-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="4e359-168">Tout le trafic de multidiffusion s’affiche désormais dans la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="4e359-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e359-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e359-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e359-170">Procédures de diagnostic WSDAPI</span><span class="sxs-lookup"><span data-stu-id="4e359-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="4e359-171">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="4e359-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




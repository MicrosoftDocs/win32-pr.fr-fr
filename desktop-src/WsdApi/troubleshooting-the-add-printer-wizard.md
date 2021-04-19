---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage de l’Assistant Ajout d’imprimante.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Résolution des problèmes liés à l’Assistant Ajout d’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521504"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="57f33-103">Résolution des problèmes liés à l’Assistant Ajout d’imprimante</span><span class="sxs-lookup"><span data-stu-id="57f33-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="57f33-104">Assistant Ajout d’imprimante :</span><span class="sxs-lookup"><span data-stu-id="57f33-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="57f33-105">Utilise toujours le WS-Discovery UDP pour la découverte des appareils</span><span class="sxs-lookup"><span data-stu-id="57f33-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="57f33-106">Lance toujours une connexion HTTP ou HTTPs pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="57f33-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="57f33-107">Utilise parfois la découverte dirigée</span><span class="sxs-lookup"><span data-stu-id="57f33-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="57f33-108">Utilise parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="57f33-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="57f33-109">Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à l’Assistant Ajout d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="57f33-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="57f33-110">**Pour résoudre les problèmes liés à l’Assistant Ajout d’imprimante**</span><span class="sxs-lookup"><span data-stu-id="57f33-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="57f33-111">Si la découverte dirigée est utilisée, [résolvez les problèmes de détection dirigée](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="57f33-112">[Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="57f33-113">[Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="57f33-114">[Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="57f33-115">[Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="57f33-116">[Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="57f33-117">[Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="57f33-118">[Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="57f33-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="57f33-119">Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57f33-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57f33-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57f33-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f33-121">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="57f33-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="57f33-122">Dépannage des applications à l’aide de la découverte dirigée</span><span class="sxs-lookup"><span data-stu-id="57f33-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 




---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage de l’Explorateur réseau.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Résolution des problèmes de l’Explorateur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951167"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="32924-103">Résolution des problèmes de l’Explorateur réseau</span><span class="sxs-lookup"><span data-stu-id="32924-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="32924-104">Explorateur réseau :</span><span class="sxs-lookup"><span data-stu-id="32924-104">The Network Explorer:</span></span>

-   <span data-ttu-id="32924-105">Utilise toujours le WS-Discovery UDP pour la découverte des appareils</span><span class="sxs-lookup"><span data-stu-id="32924-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="32924-106">Lance toujours une connexion HTTP ou HTTPs pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="32924-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="32924-107">Utilise parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="32924-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="32924-108">Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à l’Explorateur réseau.</span><span class="sxs-lookup"><span data-stu-id="32924-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="32924-109">**Pour résoudre les problèmes de l’Explorateur réseau**</span><span class="sxs-lookup"><span data-stu-id="32924-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="32924-110">[Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="32924-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="32924-111">[Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="32924-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="32924-112">[Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="32924-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="32924-113">[Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="32924-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="32924-114">[Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32924-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="32924-115">[Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="32924-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="32924-116">[Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32924-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="32924-117">L’Explorateur réseau utilise la [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) pour énumérer les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="32924-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="32924-118">Pour plus d’informations sur le dépannage, consultez [Dépannage des clients de découverte de fonctions](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="32924-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="32924-119">Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32924-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32924-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32924-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32924-121">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="32924-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="32924-122">Résolution des problèmes des clients de découverte des fonctions</span><span class="sxs-lookup"><span data-stu-id="32924-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 

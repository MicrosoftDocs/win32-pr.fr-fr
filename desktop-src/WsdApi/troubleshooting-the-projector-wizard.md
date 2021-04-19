---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage de l’Assistant projecteur.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Résolution des problèmes de l’Assistant projecteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515019"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="9aaed-103">Résolution des problèmes de l’Assistant projecteur</span><span class="sxs-lookup"><span data-stu-id="9aaed-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="9aaed-104">Assistant projecteur :</span><span class="sxs-lookup"><span data-stu-id="9aaed-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="9aaed-105">Utilise toujours le WS-Discovery UDP pour la découverte des appareils</span><span class="sxs-lookup"><span data-stu-id="9aaed-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="9aaed-106">Utilise toujours HTTP pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9aaed-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="9aaed-107">Utilise parfois la découverte dirigée</span><span class="sxs-lookup"><span data-stu-id="9aaed-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="9aaed-108">Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à l’Assistant projecteur.</span><span class="sxs-lookup"><span data-stu-id="9aaed-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="9aaed-109">**Pour résoudre les problèmes de l’Assistant projecteur**</span><span class="sxs-lookup"><span data-stu-id="9aaed-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="9aaed-110">Si la découverte dirigée est utilisée, [résolvez les problèmes de détection dirigée](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="9aaed-111">[Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="9aaed-112">[Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="9aaed-113">[Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="9aaed-114">[Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="9aaed-115">[Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="9aaed-116">[Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="9aaed-117">[Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="9aaed-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="9aaed-118">Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9aaed-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aaed-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9aaed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aaed-120">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="9aaed-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




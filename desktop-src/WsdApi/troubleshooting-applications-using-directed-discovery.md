---
description: Les applications qui utilisent la découverte dirigée envoient des messages de sondage via HTTP ou HTTPs pour découvrir des appareils.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Dépannage des applications WSDAPI à l’aide de la découverte dirigée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528575"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="e965d-103">Dépannage des applications WSDAPI à l’aide de la découverte dirigée</span><span class="sxs-lookup"><span data-stu-id="e965d-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="e965d-104">Les applications qui utilisent la découverte dirigée envoient des messages de [sondage](probe-message.md) via HTTP ou HTTPS pour découvrir des appareils.</span><span class="sxs-lookup"><span data-stu-id="e965d-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="e965d-105">Les messages [messages ProbeMatches](probematches-message.md) correspondants envoyés en réponse sont également envoyés via HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e965d-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="e965d-106">La découverte dirigée peut être lancée par l’Assistant Ajout d’imprimante, un client de découverte de fonction ou une application WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e965d-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="e965d-107">Les messages de sonde et messages ProbeMatches sont structurellement identiques à ceux envoyés via UDP.</span><span class="sxs-lookup"><span data-stu-id="e965d-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="e965d-108">Les messages sont préfixés avec les en-têtes HTTP ou HTTPs appropriés.</span><span class="sxs-lookup"><span data-stu-id="e965d-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="e965d-109">Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application à l’aide de la découverte dirigée.</span><span class="sxs-lookup"><span data-stu-id="e965d-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="e965d-110">**Pour dépanner une application WSDAPI à l’aide de la découverte dirigée**</span><span class="sxs-lookup"><span data-stu-id="e965d-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="e965d-111">[Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e965d-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="e965d-112">[Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="e965d-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="e965d-113">[Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="e965d-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="e965d-114">[Inspectez les traces réseau d’une application à l’aide de la découverte dirigée](inspecting-network-traces-for-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="e965d-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="e965d-115">Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e965d-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e965d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e965d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e965d-117">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e965d-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="e965d-118">Résolution des problèmes liés à l’Assistant Ajout d’imprimante</span><span class="sxs-lookup"><span data-stu-id="e965d-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="e965d-119">Dépannage des applications WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e965d-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 




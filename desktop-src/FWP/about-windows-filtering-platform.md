---
title: À propos de la plateforme de filtrage Windows
description: La plateforme de filtrage Windows (WFP) est une plateforme de traitement du trafic réseau conçue pour remplacer les interfaces de filtrage du trafic réseau Windows XP et Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106538594"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="db2ec-103">À propos de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="db2ec-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="db2ec-104">La plateforme de filtrage Windows (WFP) est une plateforme de traitement du trafic réseau conçue pour remplacer les interfaces de filtrage du trafic réseau Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="db2ec-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="db2ec-105">La plateforme WFP se compose d’un ensemble de raccordements dans la pile réseau et d’un moteur de filtrage qui coordonne les interactions entre les piles réseau.</span><span class="sxs-lookup"><span data-stu-id="db2ec-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="db2ec-106">Composants WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="db2ec-107">Moteur de filtre</span><span class="sxs-lookup"><span data-stu-id="db2ec-107">Filter Engine</span></span>

<span data-ttu-id="db2ec-108">L’infrastructure de filtrage multicouche de base, hébergée en mode noyau et en mode utilisateur, qui remplace les modules de filtrage multiples dans le sous-système de mise en réseau Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="db2ec-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="db2ec-109">Filtre le trafic réseau sur n’importe quelle couche du système sur tous les champs de données qu’un shim peut fournir.</span><span class="sxs-lookup"><span data-stu-id="db2ec-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="db2ec-110">Implémente les filtres de « légende » en appelant des légendes pendant la classification.</span><span class="sxs-lookup"><span data-stu-id="db2ec-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="db2ec-111">Retourne des actions « autoriser » ou « bloquer » au shim qui l’a appelée pour la mise en application.</span><span class="sxs-lookup"><span data-stu-id="db2ec-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="db2ec-112">Fournit un arbitrage entre différentes sources de stratégie.</span><span class="sxs-lookup"><span data-stu-id="db2ec-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="db2ec-113">Par exemple, détermine la priorité lorsqu’une application est configurée pour sécuriser tout le trafic réseau qui lui est associé, mais que le pare-feu local est configuré pour empêcher le trafic sécurisé des applications.</span><span class="sxs-lookup"><span data-stu-id="db2ec-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="db2ec-114">Moteur de filtrage de base (BFE)</span><span class="sxs-lookup"><span data-stu-id="db2ec-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="db2ec-115">Service qui contrôle le fonctionnement de la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="db2ec-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="db2ec-116">Il effectue les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="db2ec-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="db2ec-117">Accepte des filtres et d’autres paramètres de configuration pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="db2ec-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="db2ec-118">Indique l’état actuel du système, y compris les statistiques.</span><span class="sxs-lookup"><span data-stu-id="db2ec-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="db2ec-119">Applique le modèle de sécurité pour accepter la configuration dans la plateforme.</span><span class="sxs-lookup"><span data-stu-id="db2ec-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="db2ec-120">Par exemple, un administrateur local peut ajouter des filtres, mais les autres utilisateurs peuvent uniquement les afficher.</span><span class="sxs-lookup"><span data-stu-id="db2ec-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="db2ec-121">Raccorde les paramètres de configuration à d’autres modules dans le système.</span><span class="sxs-lookup"><span data-stu-id="db2ec-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="db2ec-122">Par exemple, les stratégies de négociation IPsec accèdent aux modules de génération de clés IKE/AuthIP, les filtres sont dirigés vers le moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="db2ec-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="db2ec-123">Shims</span><span class="sxs-lookup"><span data-stu-id="db2ec-123">Shims</span></span>

<span data-ttu-id="db2ec-124">Composants en mode noyau qui résident entre la pile réseau et le moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="db2ec-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="db2ec-125">Les shims assurent la décision de filtrage en classant par rapport au moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="db2ec-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="db2ec-126">La liste suivante répertorie les shims disponibles.</span><span class="sxs-lookup"><span data-stu-id="db2ec-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="db2ec-127">Shim de mise en application de la couche application (ALE).</span><span class="sxs-lookup"><span data-stu-id="db2ec-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="db2ec-128">Shim de module de couche de transport.</span><span class="sxs-lookup"><span data-stu-id="db2ec-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="db2ec-129">Shim du module de couche réseau.</span><span class="sxs-lookup"><span data-stu-id="db2ec-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="db2ec-130">Shim d’erreur ICMP (Internet Control Message Protocol).</span><span class="sxs-lookup"><span data-stu-id="db2ec-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="db2ec-131">Ignorer le shim.</span><span class="sxs-lookup"><span data-stu-id="db2ec-131">Discard shim.</span></span>
-   <span data-ttu-id="db2ec-132">Shim de flux.</span><span class="sxs-lookup"><span data-stu-id="db2ec-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="db2ec-133">Légendes</span><span class="sxs-lookup"><span data-stu-id="db2ec-133">Callouts</span></span>

<span data-ttu-id="db2ec-134">Ensemble de fonctions exposées par un pilote et utilisées pour le filtrage spécialisé.</span><span class="sxs-lookup"><span data-stu-id="db2ec-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="db2ec-135">Outre les actions de base de « autoriser » et « bloquer », les légendes peuvent modifier et sécuriser le trafic réseau entrant et sortant.</span><span class="sxs-lookup"><span data-stu-id="db2ec-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="db2ec-136">Pour plus d’informations sur les légendes, consultez la rubrique [pilotes Windows de la plateforme de filtrage Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) dans la documentation du kit de pilotes Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="db2ec-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="db2ec-137">WFP fournit des légendes intégrées qui effectuent les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="db2ec-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="db2ec-138">Effectuer le traitement IPsec.</span><span class="sxs-lookup"><span data-stu-id="db2ec-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="db2ec-139">Ajuster le comportement de filtrage avec état.</span><span class="sxs-lookup"><span data-stu-id="db2ec-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="db2ec-140">Effectue le filtrage en mode furtif (suppression silencieuse des paquets qui n’ont pas été demandés).</span><span class="sxs-lookup"><span data-stu-id="db2ec-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="db2ec-141">Contrôlez le déchargement TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="db2ec-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="db2ec-142">Interagissez avec le service Teredo.</span><span class="sxs-lookup"><span data-stu-id="db2ec-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="db2ec-143">Le moteur de filtre permet aux légendes tierces de s’inscrire à chacune de ses couches en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="db2ec-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="db2ec-144">Interface de programmation d’applications</span><span class="sxs-lookup"><span data-stu-id="db2ec-144">Application Programming Interface</span></span>

<span data-ttu-id="db2ec-145">Ensemble de types de données et de fonctions accessibles aux développeurs pour créer et gérer des applications de filtrage réseau.</span><span class="sxs-lookup"><span data-stu-id="db2ec-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="db2ec-146">Ces types de données et fonctions sont regroupés en plusieurs [ensembles d’API](api-sets.md).</span><span class="sxs-lookup"><span data-stu-id="db2ec-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="db2ec-147">Fonctionnalités WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-147">WFP Features</span></span>

-   <span data-ttu-id="db2ec-148">Fournit une infrastructure de filtrage de paquets dans laquelle les éditeurs de logiciels indépendants (ISV) peuvent intégrer des modules de filtrage spécialisés.</span><span class="sxs-lookup"><span data-stu-id="db2ec-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="db2ec-149">Fonctionne avec IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="db2ec-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="db2ec-150">Permet le filtrage, la modification et la réinjection des données.</span><span class="sxs-lookup"><span data-stu-id="db2ec-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="db2ec-151">Effectue le traitement des paquets et du flux.</span><span class="sxs-lookup"><span data-stu-id="db2ec-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="db2ec-152">Autorise l’activation du filtrage des paquets par application, par utilisateur et par connexion en plus de par interface réseau ou par port.</span><span class="sxs-lookup"><span data-stu-id="db2ec-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="db2ec-153">Fournit la sécurité au moment du démarrage jusqu’au démarrage du moteur de filtrage de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="db2ec-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="db2ec-154">Active le filtrage avec état des connexions.</span><span class="sxs-lookup"><span data-stu-id="db2ec-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="db2ec-155">Gère à la fois les données chiffrées avant et après IPsec.</span><span class="sxs-lookup"><span data-stu-id="db2ec-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="db2ec-156">Permet l’intégration des stratégies IPsec et de filtrage du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="db2ec-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="db2ec-157">Fournit une infrastructure de gestion des stratégies pour déterminer quand des filtres spécifiques doivent être activés.</span><span class="sxs-lookup"><span data-stu-id="db2ec-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="db2ec-158">Cela comprend la médiation des exigences conflictuelles à partir de plusieurs filtres fournis par différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="db2ec-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="db2ec-159">Gère la plupart du réassemblage de paquets et du suivi de l’État.</span><span class="sxs-lookup"><span data-stu-id="db2ec-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="db2ec-160">Comprend un système de notification utilisateur générique qui informe les abonnés des modifications apportées au système de filtrage.</span><span class="sxs-lookup"><span data-stu-id="db2ec-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="db2ec-161">Implémente des fonctions d’énumération qui signalent l’état du système.</span><span class="sxs-lookup"><span data-stu-id="db2ec-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="db2ec-162">Utilise les événements net pour enregistrer les erreurs IPsec et les rejets de paquets.</span><span class="sxs-lookup"><span data-stu-id="db2ec-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="db2ec-163">Prend en charge une [classe d’assistance NDF (](/windows/desktop/NDF/extensible-helper-classes)Network Diagnostics Framework).</span><span class="sxs-lookup"><span data-stu-id="db2ec-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="db2ec-164">Prend en charge les [extensions de socket sécurisées](/windows/desktop/WinSock/winsock-secure-socket-extensions) pour l’API Winsock, qui permettent aux applications réseau de sécuriser leur trafic en configurant WFP.</span><span class="sxs-lookup"><span data-stu-id="db2ec-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="db2ec-165">Au niveau des couches de mise en application de la couche d’application (ALE), a un impact minimal sur les performances du réseau en traitant uniquement le premier paquet dans une connexion.</span><span class="sxs-lookup"><span data-stu-id="db2ec-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="db2ec-166">Intègre le déchargement matériel où les modules de légende en mode noyau peuvent utiliser le matériel pour effectuer une inspection de paquets spécifique.</span><span class="sxs-lookup"><span data-stu-id="db2ec-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db2ec-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db2ec-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db2ec-168">Architecture WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="db2ec-169">Opération WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="db2ec-170">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="db2ec-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="db2ec-171">Configuration IPsec</span><span class="sxs-lookup"><span data-stu-id="db2ec-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="db2ec-172">Configuration de WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="db2ec-173">Surveillance de WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="db2ec-174">API WFP</span><span class="sxs-lookup"><span data-stu-id="db2ec-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 


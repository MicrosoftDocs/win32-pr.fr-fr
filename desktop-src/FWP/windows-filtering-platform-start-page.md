---
title: Plateforme de filtrage Windows
description: La plateforme de filtrage Windows (WFP) est un ensemble de services système et d’API qui fournissent une plate-forme pour la création d’applications de filtrage réseau.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plateforme de filtrage Windows
- Page de démarrage de la plateforme de filtrage Windows, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106511913"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="1c8ba-105">Plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="1c8ba-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="1c8ba-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="1c8ba-106">Purpose</span></span>

<span data-ttu-id="1c8ba-107">La plateforme de filtrage Windows (WFP) est un ensemble de services système et d’API qui fournissent une plate-forme pour la création d’applications de filtrage réseau.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="1c8ba-108">L'API WFP permet aux développeurs d'écrire du code qui interagit avec le traitement de paquets qui a lieu au niveau de plusieurs couches dans la pile de mise en réseau du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="1c8ba-109">Les données de réseau peuvent être filtrées et peuvent également être modifiées avant qu'elles atteignent leur destination.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="1c8ba-110">En fournissant une plateforme de développement plus simple, WFP est conçu pour remplacer les technologies de filtrage de paquets précédentes, telles que les filtres d’interface TDI (TDI), les filtres NDIS (Network Driver Interface Specification) et les fournisseurs de services en couche (LSP) Winsock.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="1c8ba-111">À compter de Windows Server 2008 et Windows Vista, le hook de pare-feu et les pilotes de raccordement de filtre ne sont pas disponibles. les applications qui utilisaient ces pilotes doivent à la place utiliser WFP.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="1c8ba-112">Avec l’API WFP, les développeurs peuvent implémenter des pare-feu, des systèmes de détection d’intrusion, des antivirus, des outils d’analyse réseau et des contrôles de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="1c8ba-113">WFP s’intègre à et assure la prise en charge des fonctionnalités de pare-feu, telles que la communication authentifiée et la configuration de pare-feu dynamique basée sur l’utilisation par les applications de l’API de Sockets (stratégie basée sur l’application).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="1c8ba-114">WFP fournit également l’infrastructure pour la gestion des stratégies IPsec, les notifications de modifications, les diagnostics réseau et le filtrage avec état.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="1c8ba-115">La plateforme de filtrage Windows est une plateforme de développement et non un pare-feu lui-même.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="1c8ba-116">L’application de pare-feu intégrée à Windows Vista, Windows Server 2008 et aux systèmes d’exploitation ultérieurs Windows Firewall with Advanced Security (WFAS) est implémentée à l’aide de WFP.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="1c8ba-117">Par conséquent, les applications développées avec l’API WFP ou l' [API WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) utilisent la logique d’arbitrage de filtrage commune qui est intégrée à WFP.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="1c8ba-118">L’API WFP se compose d’une API en mode utilisateur et d’une API en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="1c8ba-119">Cette section fournit une vue d’ensemble de l’ensemble de la plateforme WFP et décrit en détail uniquement la partie mode utilisateur de l’API WFP.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="1c8ba-120">Pour obtenir une description détaillée de l’API WFP en mode noyau, consultez l’aide en ligne de [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="1c8ba-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1c8ba-121">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="1c8ba-121">Developer audience</span></span>

<span data-ttu-id="1c8ba-122">L’API de la plateforme de filtrage Windows est conçue pour être utilisée par les programmeurs qui utilisent le logiciel de développement C/C++.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="1c8ba-123">Les programmeurs doivent être familiarisés avec les concepts de mise en réseau et la conception de systèmes utilisant des composants en mode utilisateur et en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1c8ba-124">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="1c8ba-124">Run-time requirements</span></span>

<span data-ttu-id="1c8ba-125">La plateforme de filtrage Windows est prise en charge sur les clients exécutant Windows Vista et versions ultérieures, et sur les serveurs exécutant Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="1c8ba-126">Pour plus d’informations sur les spécifications d’exécution d’un élément de programmation spécifique, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="1c8ba-127">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1c8ba-127">In this section</span></span>



| <span data-ttu-id="1c8ba-128">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1c8ba-128">Topic</span></span>                                                                                               | <span data-ttu-id="1c8ba-129">Description</span><span class="sxs-lookup"><span data-stu-id="1c8ba-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c8ba-130">Nouveautés de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="1c8ba-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="1c8ba-131">Informations sur les nouvelles fonctionnalités et les nouvelles API de la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="1c8ba-132">À propos de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="1c8ba-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1c8ba-133">Vue d’ensemble de la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="1c8ba-134">Utilisation de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="1c8ba-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1c8ba-135">Exemple de code utilisant l’API de la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="1c8ba-136">Informations de référence sur l’API de plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="1c8ba-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="1c8ba-137">Documentation pour les fonctions, structures et constantes de la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8ba-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="1c8ba-138">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1c8ba-138">Additional resources</span></span>

<span data-ttu-id="1c8ba-139">Pour poser des questions et avoir des discussions sur l’utilisation de l’API WFP, visitez le Forum sur la [plateforme de filtrage Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="1c8ba-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c8ba-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c8ba-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8ba-141">API de plateforme de filtrage Windows en mode noyau-Guide de conception</span><span class="sxs-lookup"><span data-stu-id="1c8ba-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="1c8ba-142">API de la plateforme de filtrage Windows en mode noyau-référence</span><span class="sxs-lookup"><span data-stu-id="1c8ba-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="1c8ba-143">Pare-feu Windows avec fonctions avancées de sécurité</span><span class="sxs-lookup"><span data-stu-id="1c8ba-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="1c8ba-144">Classe d’assistance extensible pour les diagnostics WFP</span><span class="sxs-lookup"><span data-stu-id="1c8ba-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="1c8ba-145">Extensions Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="1c8ba-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 


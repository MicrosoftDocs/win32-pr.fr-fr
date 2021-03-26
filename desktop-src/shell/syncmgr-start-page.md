---
description: Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur portable ou sur un ordinateur connecté à un réseau local.
title: gestionnaire de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991616"
---
# <a name="synchronization-manager"></a><span data-ttu-id="722c1-103">gestionnaire de synchronisation</span><span class="sxs-lookup"><span data-stu-id="722c1-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="722c1-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="722c1-104">Purpose</span></span>

<span data-ttu-id="722c1-105">Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur portable ou sur un ordinateur connecté à un réseau local.</span><span class="sxs-lookup"><span data-stu-id="722c1-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="722c1-106">Avec les fonctions de connectivité, les notifications (service de notification d’événements système) et la mise en cache côté client, le gestionnaire de synchronisation fournit une infrastructure pour prendre en charge l’informatique mobile.</span><span class="sxs-lookup"><span data-stu-id="722c1-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="722c1-107">Au lieu que chaque application implémente sa propre technologie pour mettre en cache et synchroniser les ressources réseau pour une utilisation locale, le système d’exploitation fournit un modèle intégré que toutes les applications peuvent utiliser.</span><span class="sxs-lookup"><span data-stu-id="722c1-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="722c1-108">Les fichiers sont synchronisés indépendamment du protocole.</span><span class="sxs-lookup"><span data-stu-id="722c1-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="722c1-109">Par exemple, un programme de messagerie peut transférer ses messages à l’aide du protocole SMTP, NMTP ou POP3, tandis qu’un navigateur peut utiliser le protocole HTTP, et une base de données peut utiliser l’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="722c1-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="722c1-110">Les développeurs peuvent utiliser l’interface commune au gestionnaire de synchronisation dans leurs applications pour synchroniser les fichiers entre l’ordinateur local de l’utilisateur et le stockage réseau.</span><span class="sxs-lookup"><span data-stu-id="722c1-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="722c1-111">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="722c1-111">Where applicable</span></span>

<span data-ttu-id="722c1-112">Le gestionnaire de synchronisation est destiné aux applications qui s’exécutent principalement sur des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="722c1-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="722c1-113">Les applications qui s’exécutent sur des ordinateurs connectés à des réseaux locaux à latence élevée peuvent également tirer parti de l’utilisation du gestionnaire de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="722c1-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="722c1-114">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="722c1-114">Developer audience</span></span>

<span data-ttu-id="722c1-115">Ce document est destiné aux développeurs de logiciels qui développent des applications pour l’informatique mobile et des réseaux locaux à latence élevée.</span><span class="sxs-lookup"><span data-stu-id="722c1-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="722c1-116">Ce document fournit une référence complète de toutes les parties du gestionnaire de synchronisation, y compris les méthodes et les interfaces du gestionnaire de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="722c1-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="722c1-117">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="722c1-117">Run-time requirements</span></span>

<span data-ttu-id="722c1-118">Requiert Windows Server 2003, Windows XP, Windows 2000 ou Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="722c1-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="722c1-119">Également disponible en tant que redistribuable pour Microsoft Windows NT 4,0, Windows 98 et Windows 95.</span><span class="sxs-lookup"><span data-stu-id="722c1-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="722c1-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="722c1-120">In this section</span></span>



| <span data-ttu-id="722c1-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="722c1-121">Topic</span></span>                                                                                       | <span data-ttu-id="722c1-122">Description</span><span class="sxs-lookup"><span data-stu-id="722c1-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="722c1-123">À propos du gestionnaire de synchronisation</span><span class="sxs-lookup"><span data-stu-id="722c1-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="722c1-124">Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="722c1-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="722c1-125">Configurations de l’informatique mobile</span><span class="sxs-lookup"><span data-stu-id="722c1-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="722c1-126">Les applications peuvent utiliser le gestionnaire de synchronisation pour conserver les fichiers et les ressources mis en cache localement et synchronisés sur les ordinateurs de bureau et mobiles.</span><span class="sxs-lookup"><span data-stu-id="722c1-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="722c1-127">Scénarios d’application</span><span class="sxs-lookup"><span data-stu-id="722c1-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="722c1-128">Applications et services pouvant utiliser le gestionnaire de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="722c1-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="722c1-129">Architecture du gestionnaire de synchronisation</span><span class="sxs-lookup"><span data-stu-id="722c1-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="722c1-130">Utilisation du gestionnaire de synchronisation à partir d’un programme</span><span class="sxs-lookup"><span data-stu-id="722c1-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="722c1-131">Informations de référence sur le gestionnaire de synchronisation</span><span class="sxs-lookup"><span data-stu-id="722c1-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="722c1-132">Les éléments de programmation suivants composent l’API pour le gestionnaire de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="722c1-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="722c1-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="722c1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="722c1-134">À propos du service de notification d’événements système</span><span class="sxs-lookup"><span data-stu-id="722c1-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 

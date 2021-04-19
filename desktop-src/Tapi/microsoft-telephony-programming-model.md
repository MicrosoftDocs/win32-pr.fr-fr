---
description: Le modèle de programmation de téléphonie de Microsoft permet d’extraire le contrôle des communications du contrôle de périphérique, de libérer les applications et les fabricants d’appareils des utilisateurs finaux des besoins en mars dans échelons.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modèle de programmation de téléphonie Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514373"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="85470-103">Modèle de programmation de téléphonie Microsoft</span><span class="sxs-lookup"><span data-stu-id="85470-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="85470-104">Le modèle de programmation de téléphonie de Microsoft permet d’extraire le contrôle des communications du contrôle de périphérique, de libérer les applications et les fabricants d’appareils des utilisateurs finaux des besoins en mars dans échelons.</span><span class="sxs-lookup"><span data-stu-id="85470-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="85470-105">À l’aide de ce modèle, une application de serveur ou d’utilisateur final ne requiert pas d’informations détaillées sur le contrôle de périphérique et l’appareil n’a pas besoin d’être adapté à l’application.</span><span class="sxs-lookup"><span data-stu-id="85470-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="85470-106">Les applications et les appareils peuvent subir des innovations et changer sans que cela ne soit pas rendu superflu aux clients.</span><span class="sxs-lookup"><span data-stu-id="85470-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="85470-107">Le diagramme suivant illustre la façon dont cette abstraction est accomplie.</span><span class="sxs-lookup"><span data-stu-id="85470-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![Comment l’interface TAPI isole le contrôle des communications du contrôle de périphérique](images/tapicomp.png)

<span data-ttu-id="85470-109">Ces composants peuvent être affichés en tant que référentiels de connaissances spécialisées.</span><span class="sxs-lookup"><span data-stu-id="85470-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="85470-110">L’application TAPI (Telephony Application Programming Interface) connaît les besoins des utilisateurs, la DLL TAPI et TAPISRV comprennent la téléphonie générale, et les fournisseurs de services (TSP et MSP) connaissent le contrôle détaillé de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="85470-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="85470-111">Les créateurs d’applications et les fabricants de périphériques n’ont besoin que d’une connaissance générale des exigences des autres.</span><span class="sxs-lookup"><span data-stu-id="85470-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="85470-112">Une application charge la DLL TAPI dans son espace de processus et utilise l’interface TAPI pour communiquer les besoins.</span><span class="sxs-lookup"><span data-stu-id="85470-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="85470-113">L’interface TAPI établit une communication de liaison RPC avec le serveur TAPI.</span><span class="sxs-lookup"><span data-stu-id="85470-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="85470-114">En outre, TAPI 3. x crée un objet MSP et communique avec lui à l’aide d’un ensemble de commandes défini, l’interface MSPI (Media Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="85470-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="85470-115">Quand une application appelle une opération TAPI, la bibliothèque de liens dynamiques TAPI valide et marshale les paramètres, puis transfère les informations à TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="85470-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="85470-116">TAPISRV effectue le suivi des ressources de communication disponibles sur l’ordinateur local et des interfaces avec les fournisseurs de services de téléphonie (TSPs) à l’aide de l’interface du fournisseur de services de téléphonie (TSPI).</span><span class="sxs-lookup"><span data-stu-id="85470-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="85470-117">Les communications entre un TSP et un MSP s’effectuent à l’aide d’une connexion virtuelle qui passe par la DLL TAPI et TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="85470-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="85470-118">La paire TSP/MSP fournit des informations sur l’État et les fonctionnalités de l’appareil et implémente les commandes spécifiques requises pour la réponse souhaitée.</span><span class="sxs-lookup"><span data-stu-id="85470-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="85470-119">Le résultat de l’utilisation de ce modèle de programmation est que les applications peuvent ignorer ou ajuster aux modifications des appareils et que de nouveaux appareils peuvent être utilisés instantanément au lieu d’attendre les modifications de base du code.</span><span class="sxs-lookup"><span data-stu-id="85470-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="85470-120">La part de marché potentielle est étendue pour les rédacteurs d’applications et les fabricants de périphériques.</span><span class="sxs-lookup"><span data-stu-id="85470-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="85470-121">Les rubriques suivantes décrivent les composants de téléphonie Microsoft plus en détail :</span><span class="sxs-lookup"><span data-stu-id="85470-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="85470-122">Applications TAPI</span><span class="sxs-lookup"><span data-stu-id="85470-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="85470-123">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="85470-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="85470-124">Serveur TAPI</span><span class="sxs-lookup"><span data-stu-id="85470-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="85470-125">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="85470-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="85470-126">Modèle synchrone/asynchrone</span><span class="sxs-lookup"><span data-stu-id="85470-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="85470-127">Structures de données TAPI</span><span class="sxs-lookup"><span data-stu-id="85470-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="85470-128">Niveaux de service TAPI</span><span class="sxs-lookup"><span data-stu-id="85470-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 




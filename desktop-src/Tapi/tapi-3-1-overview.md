---
description: TAPI version 3,1 est une API COM qui fusionne les téléphonie classiques et IP. Les applications possibles sont comprises entre les appels vocaux simples sur le réseau téléphonique commuté public et la multidiffusion des conférences IP multimédias avec la qualité de service (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Vue d’ensemble de TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519102"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="ce11e-104">Vue d’ensemble de TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="ce11e-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="ce11e-105">TAPI version 3,1 est une API COM qui fusionne les téléphonie classiques et IP.</span><span class="sxs-lookup"><span data-stu-id="ce11e-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="ce11e-106">Les applications possibles sont comprises entre les appels vocaux simples sur le réseau téléphonique commuté public et la multidiffusion des conférences IP multimédias avec la qualité de service (QOS).</span><span class="sxs-lookup"><span data-stu-id="ce11e-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="ce11e-107">Pour plus d’informations sur les fonctionnalités de téléphonie IP TAPI 3,1, consultez le livre blanc « téléphonie IP avec TAPI 3 », qui se trouve sur le site Web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce11e-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="ce11e-108">Il existe quatre principaux composants pour TAPI 3,1 :</span><span class="sxs-lookup"><span data-stu-id="ce11e-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="ce11e-109">API COM</span><span class="sxs-lookup"><span data-stu-id="ce11e-109">COM API</span></span>
-   <span data-ttu-id="ce11e-110">Serveur TAPI</span><span class="sxs-lookup"><span data-stu-id="ce11e-110">TAPI Server</span></span>
-   <span data-ttu-id="ce11e-111">Fournisseurs de services de téléphonie (TSPs)</span><span class="sxs-lookup"><span data-stu-id="ce11e-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="ce11e-112">Fournisseurs de flux de médias (MSP)</span><span class="sxs-lookup"><span data-stu-id="ce11e-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="ce11e-113">Le diagramme suivant illustre l’architecture TAPI 3,1 :</span><span class="sxs-lookup"><span data-stu-id="ce11e-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![architecture TAPI 3](images/callarc-gif-1.png)

<span data-ttu-id="ce11e-115">L’API est implémentée en tant que suite d’objets COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="ce11e-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="ce11e-116">Le déplacement de l’interface TAPI vers le modèle COM orienté objet permet aux développeurs d’écrire des applications compatibles TAPI dans de nombreux langages, tels que Java, Visual Basic ou C/C++.</span><span class="sxs-lookup"><span data-stu-id="ce11e-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="ce11e-117">L’utilisation de COM active les mises à niveau de composants des fonctionnalités TAPI.</span><span class="sxs-lookup"><span data-stu-id="ce11e-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="ce11e-118">Le processus de serveur TAPI (TAPISRV) extrait l’interface du fournisseur de services (TSPI) TAPI des 3. x et TAPI 2. x, ce qui permet d’utiliser les fournisseurs de services de téléphonie TAPI 2. x avec TAPI 3. x, en conservant l’état interne de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="ce11e-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="ce11e-119">TAPISRV est implémenté en tant que processus de service dans SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="ce11e-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="ce11e-120">Les [fournisseurs de services](./tapi-service-providers.md) dérésument les mécanismes de transport de médias spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ce11e-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="ce11e-121">Ils existent généralement par paires : un fournisseur de services de téléphonie (TSP) pour le contrôle d’appel et un fournisseur de services de média (MSP) pour le contrôle de média.</span><span class="sxs-lookup"><span data-stu-id="ce11e-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="ce11e-122">Les [fournisseurs de services de téléphonie](./telephony-service-providers-start-page.md) (TSPs) sont responsables de la résolution du modèle d’appel indépendant du protocole de l’interface TAPI en mécanismes de contrôle d’appels spécifiques au protocole.</span><span class="sxs-lookup"><span data-stu-id="ce11e-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="ce11e-123">TAPI 3,1 offre une compatibilité descendante avec TAPI 2,1 TSPs.</span><span class="sxs-lookup"><span data-stu-id="ce11e-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="ce11e-124">Deux fournisseurs de services de téléphonie IP (et leurs MSP associés) sont livrés par défaut avec TAPI 3,1 : le TSP H. 323 et le TSP de conférence IP multicast.</span><span class="sxs-lookup"><span data-stu-id="ce11e-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="ce11e-125">Les [fournisseurs de services multimédias](media-service-providers-start-page.md) (MSP) offrent un moyen uniforme d’accéder aux flux de média dans un appel, en prenant en charge l’API DirectShow<sup>TM</sup> comme gestionnaire de flux de média principal.</span><span class="sxs-lookup"><span data-stu-id="ce11e-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="ce11e-126">Les MSP TAPI implémentent des interfaces DirectShow pour un TSP particulier et sont requis pour tout service de téléphonie qui utilise la diffusion en continu DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ce11e-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="ce11e-127">Les flux génériques sont gérés par l’application.</span><span class="sxs-lookup"><span data-stu-id="ce11e-127">Generic streams are handled by the application.</span></span>

 

 

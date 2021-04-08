---
description: Les contrôles de média et d’appel TAPI 3 sont un ensemble générique d’objets COM, d’interfaces et de méthodes permettant d’effectuer des appels entre deux machines ou plus.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: À propos des contrôles Call et Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869565"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="091f4-103">À propos des contrôles Call et Media</span><span class="sxs-lookup"><span data-stu-id="091f4-103">About Call And Media Controls</span></span>

<span data-ttu-id="091f4-104">Les contrôles de média et d’appel TAPI 3 sont un ensemble générique d’objets COM, d’interfaces et de méthodes permettant d’effectuer des appels entre deux machines ou plus.</span><span class="sxs-lookup"><span data-stu-id="091f4-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="091f4-105">Dans le contexte de l’interface TAPI 3, l' *appel* fait référence non seulement à la transmission vocale sur le réseau public commuté (RTPC), mais aussi aux moyens et moyens de transport pour lesquels des fournisseurs de services existent : par exemple, une conférence multimédia multidiffusion s’exécutant sur un intranet d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="091f4-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="091f4-106">Les cinq objets principaux dans l’architecture d’appel et de contrôle de média TAPI 3 sont [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md)et [CallHub](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="091f4-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="091f4-107">En outre, des mises en service ont été apportées pour les [interfaces spécifiques au fournisseur](provider-specific-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="091f4-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="091f4-108">Le diagramme suivant illustre la façon dont ces objets interagissent.</span><span class="sxs-lookup"><span data-stu-id="091f4-108">The following diagram illustrates how these objects interact.</span></span>

![interactions entre les objets TAPI 3,0 Call et les objets MCI](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="091f4-110">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="091f4-110">Features</span></span>

-   <span data-ttu-id="091f4-111">Fait abstraction des fonctionnalités d’appel et de support pour permettre aux protocoles de communication différents et apparemment incompatibles d’exposer une interface commune aux applications.</span><span class="sxs-lookup"><span data-stu-id="091f4-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="091f4-112">Basé sur le modèle COM (Component Object Model), les applications peuvent être écrites dans pratiquement n’importe quel langage.</span><span class="sxs-lookup"><span data-stu-id="091f4-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="091f4-113">Si vous avez besoin d’informations supplémentaires sur COM, consultez le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="091f4-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="091f4-114">Contrôle d’appel fourni par les fournisseurs de services de téléphonie (TSPs), qui implémentent des mécanismes spécifiques au transport.</span><span class="sxs-lookup"><span data-stu-id="091f4-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="091f4-115">Contrôle multimédia fourni par les fournisseurs de services de média (MSP).</span><span class="sxs-lookup"><span data-stu-id="091f4-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="091f4-116">Les MSP actuels utilisent DirectShow.</span><span class="sxs-lookup"><span data-stu-id="091f4-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="091f4-117">DirectShow est un système modulaire de composants enfichables appelés filtres, organisés dans une configuration appelée graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="091f4-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="091f4-118">Le gestionnaire de graphique de filtre supervise la connexion de ces filtres et contrôle le flux de données du flux.</span><span class="sxs-lookup"><span data-stu-id="091f4-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="091f4-119">Si vous avez besoin d’informations supplémentaires sur DirectShow, consultez le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="091f4-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 




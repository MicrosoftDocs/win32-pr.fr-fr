---
description: Un fournisseur de services multimédia (MSP) TAPI 3 permet à une application un contrôle considérable sur les supports pour un mécanisme de transport particulier.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: À propos du fournisseur de services multimédia (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116038"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="4782e-103">À propos du fournisseur de services multimédia (MSP)</span><span class="sxs-lookup"><span data-stu-id="4782e-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="4782e-104">Un fournisseur de services multimédia (MSP) TAPI 3 permet à une application un contrôle considérable sur les supports pour un mécanisme de transport particulier.</span><span class="sxs-lookup"><span data-stu-id="4782e-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="4782e-105">Un MSP existe toujours associé à un fournisseur de services de téléphonie (TSP).</span><span class="sxs-lookup"><span data-stu-id="4782e-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="4782e-106">Tout comme un TSP est une couche d’abstraction pour le contrôle d’appel, le MSP contrôle les médias sans avoir besoin de codage spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4782e-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="4782e-107">Pour obtenir un exemple de communication MSP/TSP, consultez [vue d’ensemble du fournisseur de services TAPI](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4782e-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="4782e-108">Un MSP permet le contrôle multimédia via l’utilisation d’interfaces de terminal, de flux et de sous-flux spéciales définies par l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="4782e-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="4782e-109">Le diagramme dans [à propos des contrôles d’appel et des médias](about-call-and-media-controls.md) illustre la façon dont ces interfaces apparaissent dans une application TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="4782e-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="4782e-110">En outre, un MSP peut implémenter des [interfaces privées spécifiques au fournisseur](provider-specific-interfaces.md), que l’interface TAPI regroupera sur les objets standard exposés à une application.</span><span class="sxs-lookup"><span data-stu-id="4782e-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="4782e-111">Par exemple, Microsoft IPConf MSP, qui est installé avec Microsoft Windows 2000, implémente l’interface [**ITParticipant**](itparticipant.md) , qui fournit des contrôles pour les membres individuels d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="4782e-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="4782e-112">La rubrique suivante décrit brièvement les MSP qui peuvent être installés avec un système d’exploitation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4782e-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="4782e-113">Pour plus d’informations sur la configuration et l’utilisation, consultez le kit de ressources pour la plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="4782e-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="4782e-114">D’autres fournisseurs de services multimédias tiers peuvent être écrits pour des protocoles particuliers ou pour des appareils physiques.</span><span class="sxs-lookup"><span data-stu-id="4782e-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="4782e-115">L' [interface MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-.md) décrit les interfaces qui doivent être implémentées pour permettre à un MSP d’interagir avec les composants de Microsoft Telephony.</span><span class="sxs-lookup"><span data-stu-id="4782e-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 

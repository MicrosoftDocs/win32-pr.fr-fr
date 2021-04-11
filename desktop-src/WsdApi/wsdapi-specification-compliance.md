---
description: L’API WSDAPI (Web Services on Devices) assure la prise en charge du profil des appareils pour les services Web (DPWS) sous Windows Vista, qui permet la communication des services Web (WS) entre les ordinateurs Windows et les périphériques connectés au réseau.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformité de la spécification WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202992"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="ea5e5-103">Conformité de la spécification WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ea5e5-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="ea5e5-104">L’API WSDAPI (Web Services on Devices) assure la prise en charge du [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) sous Windows Vista, qui permet la communication des services Web (WS) entre les ordinateurs Windows et les périphériques connectés au réseau.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="ea5e5-105">DPWS assemble des spécifications WS de base, telles que [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)et [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), et les améliore ou les limite pour fournir un ensemble de fonctionnalités de base pour les appareils à ressources restreintes.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="ea5e5-106">Cette spécification de base contient les fonctionnalités requises, telles que la possibilité de décrire les propriétés de l’appareil via des métadonnées et des fonctionnalités facultatives, telles que la possibilité de rejeter des messages spécifiques pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="ea5e5-107">L’implémentation du WSDAPI dans Windows Vista est la première version de la prise en charge explicite de DPWS, et est une implémentation non managée de DPWS qui est distincte et distincte des autres implémentations de services Web (telles que le [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span><span class="sxs-lookup"><span data-stu-id="ea5e5-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="ea5e5-108">Les rubriques suivantes présentent un intérêt pour les fabricants de périphériques et les autres implémenteurs d’appareils qui créent des appareils qui interagissent avec les clients et hôtes WSDAPI basés sur Windows sans utiliser WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="ea5e5-109">Ces rubriques décrivent l’implémentation de WSDAPI par rapport aux spécifications sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="ea5e5-110">Elles couvrent l’implémentation des fonctionnalités requises, des fonctionnalités facultatives et des fonctionnalités supplémentaires non définies dans la spécification.</span><span class="sxs-lookup"><span data-stu-id="ea5e5-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="ea5e5-111">Conformité de la spécification DPWS</span><span class="sxs-lookup"><span data-stu-id="ea5e5-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="ea5e5-112">Conformité de la spécification WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="ea5e5-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="ea5e5-113">Conformité des spécifications WS-MetadataExchange et WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="ea5e5-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="ea5e5-114">Fonctionnalités de WS-Discovery supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ea5e5-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="ea5e5-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea5e5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea5e5-116">Développement de périphérique WSD</span><span class="sxs-lookup"><span data-stu-id="ea5e5-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="ea5e5-117">Recommandations en matière d’implémentation des appareils WSD</span><span class="sxs-lookup"><span data-stu-id="ea5e5-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 

---
description: L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au profil des appareils pour les services Web (DPWS).
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Services Web sur les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522680"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="e3bc5-103">Services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="e3bc5-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="e3bc5-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="e3bc5-104">Purpose</span></span>

<span data-ttu-id="e3bc5-105">L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="e3bc5-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="e3bc5-106">WSDAPI utilise [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) pour la découverte des appareils.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="e3bc5-107">WSDAPI peut être utilisé pour le développement des implémentations du client et du service.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e3bc5-108">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="e3bc5-108">Where applicable</span></span>

<span data-ttu-id="e3bc5-109">Les services Web sur les appareils permettent à un client de découvrir et d’accéder à un appareil distant et à ses services associés sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="e3bc5-110">Il prend en charge la découverte, la description, le contrôle et les événements des appareils.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="e3bc5-111">Les développeurs peuvent créer des proxys de client WSDAPI et les stubs correspondants pour les hôtes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e3bc5-112">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="e3bc5-112">Developer audience</span></span>

<span data-ttu-id="e3bc5-113">La documentation sur les appareils Web services sur les appareils est destinée aux programmeurs C/C++ et aux fournisseurs d’appareils qui créent des produits conformes à DPWS.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e3bc5-114">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="e3bc5-114">Run-time requirements</span></span>

<span data-ttu-id="e3bc5-115">Les applications clientes qui utilisent WSDAPI sont prises en charge à partir de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e3bc5-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e3bc5-116">In this section</span></span>



| <span data-ttu-id="e3bc5-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e3bc5-117">Topic</span></span>                                                                                  | <span data-ttu-id="e3bc5-118">Description</span><span class="sxs-lookup"><span data-stu-id="e3bc5-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3bc5-119">À propos des services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="e3bc5-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="e3bc5-120">Informations architecturales et générales sur les services Web sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="e3bc5-121">Utilisation de services Web sur des appareils</span><span class="sxs-lookup"><span data-stu-id="e3bc5-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="e3bc5-122">Informations sur la génération de code, la configuration des applications et la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="e3bc5-123">Informations de référence sur les services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="e3bc5-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="e3bc5-124">Documentation de référence sur l’API des services Web sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="e3bc5-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="e3bc5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3bc5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3bc5-126">Blog de Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="e3bc5-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 


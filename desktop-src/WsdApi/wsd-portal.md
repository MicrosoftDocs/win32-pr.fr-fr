---
description: En savoir plus sur l’implémentation de WSD (Web Services on Devices). Comprenez son objectif, où il s’applique, l’audience du développeur et les exigences d’exécution.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Services Web sur les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405752"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="bc33a-104">Services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="bc33a-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="bc33a-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="bc33a-105">Purpose</span></span>

<span data-ttu-id="bc33a-106">L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="bc33a-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="bc33a-107">WSDAPI utilise [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) pour la découverte des appareils.</span><span class="sxs-lookup"><span data-stu-id="bc33a-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="bc33a-108">WSDAPI peut être utilisé pour le développement des implémentations du client et du service.</span><span class="sxs-lookup"><span data-stu-id="bc33a-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="bc33a-109">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="bc33a-109">Where applicable</span></span>

<span data-ttu-id="bc33a-110">Les services Web sur les appareils permettent à un client de découvrir et d’accéder à un appareil distant et à ses services associés sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="bc33a-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="bc33a-111">Il prend en charge la découverte, la description, le contrôle et les événements des appareils.</span><span class="sxs-lookup"><span data-stu-id="bc33a-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="bc33a-112">Les développeurs peuvent créer des proxys de client WSDAPI et les stubs correspondants pour les hôtes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="bc33a-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bc33a-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="bc33a-113">Developer audience</span></span>

<span data-ttu-id="bc33a-114">La documentation sur les appareils Web services sur les appareils est destinée aux programmeurs C/C++ et aux fournisseurs d’appareils qui créent des produits conformes à DPWS.</span><span class="sxs-lookup"><span data-stu-id="bc33a-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bc33a-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="bc33a-115">Run-time requirements</span></span>

<span data-ttu-id="bc33a-116">Les applications clientes qui utilisent WSDAPI sont prises en charge à partir de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bc33a-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bc33a-117">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="bc33a-117">In this section</span></span>



| <span data-ttu-id="bc33a-118">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bc33a-118">Topic</span></span>                                                                                  | <span data-ttu-id="bc33a-119">Description</span><span class="sxs-lookup"><span data-stu-id="bc33a-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc33a-120">À propos des services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="bc33a-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="bc33a-121">Informations architecturales et générales sur les services Web sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="bc33a-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="bc33a-122">Utilisation de services Web sur des appareils</span><span class="sxs-lookup"><span data-stu-id="bc33a-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="bc33a-123">Informations sur la génération de code, la configuration des applications et la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="bc33a-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="bc33a-124">Informations de référence sur les services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="bc33a-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="bc33a-125">Documentation de référence sur l’API des services Web sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="bc33a-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="bc33a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc33a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc33a-127">Blog de Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="bc33a-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 


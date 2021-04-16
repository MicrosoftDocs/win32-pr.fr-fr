---
title: Informations de référence sur l’API d’hôte d’appareil
description: Les interfaces suivantes font partie de l’API de l’hôte d’appareil avec la technologie UPnP. L’hôte d’appareil avec la technologie UPnP prend en charge Microsoft Visual Basic et C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380190"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="48f43-104">Informations de référence sur l’API d’hôte d’appareil</span><span class="sxs-lookup"><span data-stu-id="48f43-104">Device Host API Reference</span></span>

<span data-ttu-id="48f43-105">Les interfaces suivantes font partie de l’API de l’hôte d’appareil avec la technologie UPnP.</span><span class="sxs-lookup"><span data-stu-id="48f43-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="48f43-106">L’hôte d’appareil avec la technologie UPnP prend en charge Microsoft Visual Basic et C++.</span><span class="sxs-lookup"><span data-stu-id="48f43-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="48f43-107">Cette API ne prend pas en charge Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="48f43-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="48f43-108">Interface</span><span class="sxs-lookup"><span data-stu-id="48f43-108">Interface</span></span>                                                  | <span data-ttu-id="48f43-109">Description</span><span class="sxs-lookup"><span data-stu-id="48f43-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48f43-110">**IUPnPDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="48f43-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="48f43-111">Utilisé par l’hôte d’appareil pour gérer les appareils et les services associés.</span><span class="sxs-lookup"><span data-stu-id="48f43-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="48f43-112">**IUPnPDeviceProvider**</span><span class="sxs-lookup"><span data-stu-id="48f43-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="48f43-113">Utilisé par l’hôte d’appareil pour démarrer et arrêter des fournisseurs de périphériques.</span><span class="sxs-lookup"><span data-stu-id="48f43-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="48f43-114">**IUPnPEventSink**</span><span class="sxs-lookup"><span data-stu-id="48f43-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="48f43-115">Utilisé par les appareils pour envoyer des notifications d’événements à l’hôte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="48f43-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="48f43-116">**IUPnPEventSource**</span><span class="sxs-lookup"><span data-stu-id="48f43-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="48f43-117">Utilisé par l’hôte d’appareil pour s’abonner ou annuler l’abonnement aux événements fournis par le service hébergé.</span><span class="sxs-lookup"><span data-stu-id="48f43-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="48f43-118">**IUPnPRegistrar**</span><span class="sxs-lookup"><span data-stu-id="48f43-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="48f43-119">Utilisé par les appareils pour s’inscrire auprès de l’hôte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="48f43-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="48f43-120">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="48f43-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="48f43-121">Utilisé par les appareils pour obtenir des informations sur un demandeur (c’est-à-dire un point de contrôle) et la demande.</span><span class="sxs-lookup"><span data-stu-id="48f43-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="48f43-122">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="48f43-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="48f43-123">Utilisé par les appareils pour s’inscrire à nouveau auprès de l’hôte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="48f43-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 





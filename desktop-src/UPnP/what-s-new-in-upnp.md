---
title: Nouveautés des API UPnP
description: Les API de™ UPnP ont de nouvelles fonctionnalités et une documentation mise à jour pour Windows XP SP2. Le tableau suivant identifie la nouvelle documentation.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675766"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="5b27d-104">Nouveautés des API UPnP</span><span class="sxs-lookup"><span data-stu-id="5b27d-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="5b27d-105">Les API de™ UPnP ont de nouvelles fonctionnalités et une documentation mise à jour pour Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="5b27d-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="5b27d-106">Le tableau suivant identifie la nouvelle documentation.</span><span class="sxs-lookup"><span data-stu-id="5b27d-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="5b27d-107">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="5b27d-107">Feature</span></span>                                                          | <span data-ttu-id="5b27d-108">Description</span><span class="sxs-lookup"><span data-stu-id="5b27d-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b27d-109">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="5b27d-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="5b27d-110">Cette nouvelle interface permet à un appareil hébergé d’obtenir des informations sur un demandeur (autrement dit, un point de contrôle) et la demande.</span><span class="sxs-lookup"><span data-stu-id="5b27d-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="5b27d-111">Il inclut trois méthodes, chacune d’elles fournissant un type d’informations différent.</span><span class="sxs-lookup"><span data-stu-id="5b27d-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="5b27d-112">Implémentation du comportement de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5b27d-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="5b27d-113">Cette rubrique comprend une nouvelle section qui explique comment obtenir des informations de point de terminaison à l’aide de la nouvelle interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="5b27d-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="5b27d-114">Paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="5b27d-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="5b27d-115">Cette nouvelle rubrique fournit des informations sur les paramètres du Registre qui affectent le comportement des API UPnP.</span><span class="sxs-lookup"><span data-stu-id="5b27d-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="5b27d-116">Codes d’erreur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5b27d-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="5b27d-117">Cette nouvelle rubrique explique comment un code d’erreur d’un appareil est converti en valeur HRESULT et vice versa.</span><span class="sxs-lookup"><span data-stu-id="5b27d-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="5b27d-118">Une bonne compréhension de ce processus est nécessaire pour évaluer une valeur HRESULT retournée par les méthodes [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) et [**IUPnPService :: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) .</span><span class="sxs-lookup"><span data-stu-id="5b27d-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 





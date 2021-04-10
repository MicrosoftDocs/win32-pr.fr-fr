---
title: Recherche d’appareils
description: L’architecture UPnP est une architecture réseau dynamique qui permet aux appareils de rejoindre et de sortir le réseau à tout moment.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029675"
---
# <a name="finding-devices"></a><span data-ttu-id="c8a9b-103">Recherche d’appareils</span><span class="sxs-lookup"><span data-stu-id="c8a9b-103">Finding Devices</span></span>

<span data-ttu-id="c8a9b-104">L’architecture UPnP est une architecture réseau dynamique qui permet aux appareils de rejoindre et de sortir le réseau à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="c8a9b-105">En raison de cette architecture dynamique, les applications ne peuvent pas s’appuyer sur des périphériques UPnP spécifiques pour être disponibles à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="c8a9b-106">Pour cette raison, les applications (ou points de contrôle) recherchent le réseau pour trouver les appareils qui correspondent le mieux aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="c8a9b-107">Les applications attendent également des messages de publication d’appareil indiquant que de nouveaux appareils ont été ajoutés au réseau.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="c8a9b-108">Les éléments suivants sont des critères de recherche valides pour les périphériques basés sur UPnP :</span><span class="sxs-lookup"><span data-stu-id="c8a9b-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="c8a9b-109">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="c8a9b-109">Device type</span></span>
-   <span data-ttu-id="c8a9b-110">Type de service</span><span class="sxs-lookup"><span data-stu-id="c8a9b-110">Service type</span></span>
-   <span data-ttu-id="c8a9b-111">Nom d’appareil unique (UDN)</span><span class="sxs-lookup"><span data-stu-id="c8a9b-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="c8a9b-112">Tous les appareils racine</span><span class="sxs-lookup"><span data-stu-id="c8a9b-112">All root devices</span></span>

<span data-ttu-id="c8a9b-113">Le type d’appareil et les recherches de type de service sont généralement utilisés pour rechercher une classe d’appareils avec des caractéristiques communes.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="c8a9b-114">La recherche UDN est utilisée pour rechercher un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="c8a9b-115">Pour rechercher des appareils, une application doit d’abord instancier l’objet Device Finder.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="c8a9b-116">Cet objet expose l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; ses méthodes effectuent les recherches décrites précédemment.</span><span class="sxs-lookup"><span data-stu-id="c8a9b-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="c8a9b-117">Les sections suivantes décrivent le processus de recherche d’appareils :</span><span class="sxs-lookup"><span data-stu-id="c8a9b-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="c8a9b-118">Création du Finder d’appareils</span><span class="sxs-lookup"><span data-stu-id="c8a9b-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="c8a9b-119">Recherche asynchrone</span><span class="sxs-lookup"><span data-stu-id="c8a9b-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="c8a9b-120">Recherche synchrone</span><span class="sxs-lookup"><span data-stu-id="c8a9b-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="c8a9b-121">Regroupements de périphériques retournés par les recherches synchrones</span><span class="sxs-lookup"><span data-stu-id="c8a9b-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 





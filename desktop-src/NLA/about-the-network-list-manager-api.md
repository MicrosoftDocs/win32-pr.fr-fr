---
title: À propos de l’API du gestionnaire de listes de réseaux
description: À propos de l’API du gestionnaire de listes de réseaux
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675258"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="49706-103">À propos de l’API du gestionnaire de listes de réseaux</span><span class="sxs-lookup"><span data-stu-id="49706-103">About the Network List Manager API</span></span>

<span data-ttu-id="49706-104">L’environnement réseau Microsoft Windows permet aux ordinateurs multirésidents de se connecter simultanément à plusieurs réseaux.</span><span class="sxs-lookup"><span data-stu-id="49706-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="49706-105">Il peut y avoir plusieurs réseaux sans fil disponibles, ainsi que des connexions de réseau local et d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="49706-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="49706-106">Le gestionnaire de listes de réseaux identifie les réseaux disponibles et retourne les données d’attribut réseau à l’application.</span><span class="sxs-lookup"><span data-stu-id="49706-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="49706-107">L’API du gestionnaire de listes de réseaux interagit avec le service Network List Manager pour identifier et récupérer les propriétés de chaque réseau auquel le PC se connecte.</span><span class="sxs-lookup"><span data-stu-id="49706-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="49706-108">Chaque réseau est identifié de manière unique par une signature réseau basée sur les propriétés identifiables de manière unique de ce réseau.</span><span class="sxs-lookup"><span data-stu-id="49706-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="49706-109">Lorsqu’une application s’inscrit pour les notifications du gestionnaire de liste de réseaux, l’application reçoit des notifications sur la disponibilité de nouvelles connexions réseau ou des modifications apportées aux connexions réseau existantes.</span><span class="sxs-lookup"><span data-stu-id="49706-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="49706-110">Les applications peuvent ajuster leur logique en fonction du réseau auquel elles sont connectées ; la connexion réseau à laquelle ils sont connectés ; ou les propriétés du réseau.</span><span class="sxs-lookup"><span data-stu-id="49706-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="49706-111">Avec ces informations, les applications peuvent affiner leurs actions en fonction des conditions actuelles du réseau.</span><span class="sxs-lookup"><span data-stu-id="49706-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="49706-112">Windows Vista introduit de nouvelles interfaces qui peuvent être utilisées pour obtenir des informations détaillées sur ces caractéristiques du réseau, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="49706-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="49706-113">Avec l’interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) , il est facile d’énumérer tous les réseaux ([**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) qu’un ordinateur a jamais vu, ou seulement les réseaux connectés, ou uniquement les réseaux déconnectés.</span><span class="sxs-lookup"><span data-stu-id="49706-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="49706-114">L’interface **INetworkListManager** facilite également l’énumération des interfaces réseau sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="49706-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="49706-115">L’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) est utilisée pour déterminer les propriétés d’une connexion réseau : Name, description, ID, Managed/Authenticated, Connected/Disconnected, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="49706-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="49706-116">Il est possible qu’un seul réseau soit connecté à plusieurs interfaces. par conséquent, par le biais d’une interface **iNetwork** , vous pouvez également énumérer les instances de l’interface **iNetwork** utilisée.</span><span class="sxs-lookup"><span data-stu-id="49706-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="49706-117">L’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) vous indique les propriétés pertinentes d’une interface : ID, Guid, type (géré, authentifié) et État (connecté, déconnecté, v4 local, v4 Internet, V6 local, V6 Internet).</span><span class="sxs-lookup"><span data-stu-id="49706-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="49706-118">La version locale v4 signifie un accès local IPv4 (Internet Protocol version 4).</span><span class="sxs-lookup"><span data-stu-id="49706-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="49706-119">Internet v4 signifie IPv4 avec accès à Internet.</span><span class="sxs-lookup"><span data-stu-id="49706-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="49706-120">IPv6 local et V6 Internet signifiant IPv6.</span><span class="sxs-lookup"><span data-stu-id="49706-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="49706-121">La racine de l’arborescence d’objets pour l’emplacement réseau est l’interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) .</span><span class="sxs-lookup"><span data-stu-id="49706-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="49706-122">Cette interface est implémentée sur la coclasse **CLSID \_ NetworkListManager** .</span><span class="sxs-lookup"><span data-stu-id="49706-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="49706-123">Pour utiliser cette interface, il est nécessaire de créer l’objet com **CLSID \_ NetworkListManager** comme illustré ci-après :</span><span class="sxs-lookup"><span data-stu-id="49706-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 





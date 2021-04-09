---
description: Les fournisseurs de paquets réseau (NPPs) sont des composants système Moniteur réseau qui collectent le trafic réseau (trames) à partir du réseau et les transmettent à l’interface utilisateur Moniteur réseau, ainsi qu’aux applications NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Fournisseurs de paquets réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868825"
---
# <a name="network-packet-providers"></a><span data-ttu-id="ca58b-103">Fournisseurs de paquets réseau</span><span class="sxs-lookup"><span data-stu-id="ca58b-103">Network Packet Providers</span></span>

<span data-ttu-id="ca58b-104">Les fournisseurs de paquets réseau (NPPs) sont des composants système Moniteur réseau qui collectent le trafic réseau (trames) à partir du réseau et les transmettent à l’interface utilisateur Moniteur réseau, ainsi qu’aux [*applications NPP*](n.md).</span><span class="sxs-lookup"><span data-stu-id="ca58b-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="ca58b-105">L’illustration suivante montre deux NPPs : le NPP NDIS fourni par Moniteur réseau et un NPP personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ca58b-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NDIS NPP fourni par le moniteur réseau et un NPP personnalisé](images/npp.png)

<span data-ttu-id="ca58b-107">Le NPP NDIS fourni par Moniteur réseau est Ndisnpp.dll.</span><span class="sxs-lookup"><span data-stu-id="ca58b-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="ca58b-108">Ce NPP utilise le pilote de système de Moniteur réseau (Nmnt.sys) pour récupérer les trames collectées à partir du réseau et plusieurs interfaces COM (appelées interfaces NPP) pour transmettre les frames à l’interface utilisateur Moniteur réseau, et les applications NPP, où elles peuvent être affichées et analysées.</span><span class="sxs-lookup"><span data-stu-id="ca58b-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="ca58b-109">Ndisnpp.dll se connecte à la couche [*NDIS*](n.md) pour obtenir son trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="ca58b-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="ca58b-110">(Les NPPs personnalisées peuvent contourner la couche NDIS et communiquer directement avec le matériel de mise en réseau.) Sachez que, même si un NPP utilise NDIS, NPPs peut se connecter à n’importe quel nombre de cartes réseau et que tous les NPPs doivent prendre en charge les mêmes interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="ca58b-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="ca58b-111">Pour qu’une application puisse commencer à capturer des données, elle doit :</span><span class="sxs-lookup"><span data-stu-id="ca58b-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="ca58b-112">Sélectionnez la carte d’interface réseau (NIC) qui connectera le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="ca58b-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="ca58b-113">Sélectionnez l’interface NPP qui sera utilisée pour capturer les trames réseau.</span><span class="sxs-lookup"><span data-stu-id="ca58b-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="ca58b-114">Utilisez l’interface sélectionnée pour vous connecter à la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="ca58b-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="ca58b-115">Pour plus d’informations sur l’énumération et la sélection d’une carte d’interface réseau, consultez [sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md).</span><span class="sxs-lookup"><span data-stu-id="ca58b-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="ca58b-116">Pour plus d’informations sur les interfaces COM exposées par NPPs, consultez [sélection d’une interface NPP](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ca58b-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca58b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca58b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca58b-118">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="ca58b-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="ca58b-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="ca58b-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="ca58b-120">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="ca58b-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="ca58b-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="ca58b-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 




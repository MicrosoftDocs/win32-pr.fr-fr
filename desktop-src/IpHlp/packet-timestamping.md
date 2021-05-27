---
title: Horodatage des paquets
description: Les API d’horodatage des paquets d’assistance IP permettent de déterminer la capacité d’horodatage d’une carte réseau et d’interroger les horodateurs à partir de la carte réseau sous la forme d’horodateurs croisés.
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 07743473bcb606ccdb86c55f14a3413adf10d73a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559982"
---
# <a name="packet-timestamping"></a><span data-ttu-id="492c9-103">Horodatage des paquets</span><span class="sxs-lookup"><span data-stu-id="492c9-103">Packet timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="492c9-104">Introduction</span><span class="sxs-lookup"><span data-stu-id="492c9-104">Introduction</span></span>

<span data-ttu-id="492c9-105">De nombreuses cartes d’interface réseau (cartes réseau ou cartes réseau) peuvent générer un horodateur sur leur matériel chaque fois qu’un paquet est reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="492c9-105">Many network interface cards (NICs, or network adapters) can generate a timestamp in their hardware whenever a packet is received or transmitted.</span></span> <span data-ttu-id="492c9-106">L’horodateur est généré à l’aide de l’horloge matérielle de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="492c9-106">The timestamp is generated using the NIC's own hardware clock.</span></span> <span data-ttu-id="492c9-107">Cette fonctionnalité est utilisée en particulier par le protocole PTP (Precision Time Protocol), qui est un protocole de synchronisation horaire.</span><span class="sxs-lookup"><span data-stu-id="492c9-107">This feature is used in particular by the Precision Time Protocol (PTP), which is a time synchronization protocol.</span></span> <span data-ttu-id="492c9-108">PTP prévoit d’utiliser ces horodateurs matériels dans le protocole lui-même.</span><span class="sxs-lookup"><span data-stu-id="492c9-108">PTP makes provision to use such hardware timestamps within the protocol itself.</span></span>

<span data-ttu-id="492c9-109">Les horodateurs peuvent, par exemple, être utilisés pour calculer le temps passé par un paquet au sein de la pile réseau de l’ordinateur avant d’être envoyé ou reçu à partir du câble.</span><span class="sxs-lookup"><span data-stu-id="492c9-109">The timestamps can, for example, be used to compute the time spent by a packet within the network stack of the machine before being sent to or received from the wire.</span></span> <span data-ttu-id="492c9-110">Ces calculs peuvent ensuite être utilisés par PTP pour améliorer la précision de la synchronisation de l’heure.</span><span class="sxs-lookup"><span data-stu-id="492c9-110">Those calculations can then be used by PTP to improve the accuracy of time synchronization.</span></span> <span data-ttu-id="492c9-111">La prise en charge de l’horodatage des paquets des cartes réseau est parfois conçue spécifiquement pour le protocole PTP.</span><span class="sxs-lookup"><span data-stu-id="492c9-111">The packet timestamping support of network adapters is geared sometimes specifically for the PTP protocol.</span></span> <span data-ttu-id="492c9-112">Dans d’autres cas, une prise en charge plus générale est fournie.</span><span class="sxs-lookup"><span data-stu-id="492c9-112">In other cases, a more general support is provided.</span></span>

<span data-ttu-id="492c9-113">Les API d’horodatage offrent à Windows la possibilité de prendre en charge la fonction d’horodatage matériel des cartes réseau pour le protocole PTP version 2.</span><span class="sxs-lookup"><span data-stu-id="492c9-113">Timestamping APIs give Windows the ability to support the hardware timestamping capability of network adapters for the PTP version 2 protocol.</span></span> <span data-ttu-id="492c9-114">Globalement, les fonctionnalités incluent la possibilité pour les pilotes de cartes réseau de prendre en charge les horodateurs, et pour les applications en mode utilisateur de consommer les horodateurs associés aux paquets via [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (voir [horodatage Winsock](/windows/win32/winsock/winsock-timestamping)).</span><span class="sxs-lookup"><span data-stu-id="492c9-114">Overall, the features include providing the ability to drivers of network adapters to support timestamps, and for user-mode applications to consume timestamps associated with packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (see [Winsock timestamping](/windows/win32/winsock/winsock-timestamping)).</span></span> <span data-ttu-id="492c9-115">En outre, la possibilité de générer des horodateurs logicielles est également disponible, ce qui permet à un pilote réseau de générer des horodateurs dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="492c9-115">In addition, the ability to generate software timestamps is also available, which allows a network driver to generate timestamps in software.</span></span> <span data-ttu-id="492c9-116">Ces horodateurs de logiciel sont générés par les pilotes de carte réseau à l’aide de l’équivalent en mode noyau de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span><span class="sxs-lookup"><span data-stu-id="492c9-116">Such software timestamps are generated by NIC drivers using the kernel-mode equivalent of [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span></span> <span data-ttu-id="492c9-117">Toutefois, l’activation conjointe des horodateurs matériel *et* logiciel n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="492c9-117">However, having both hardware *and* software timestamps enabled together isn't supported.</span></span>

<span data-ttu-id="492c9-118">En particulier, les API d’horodatage des paquets de l’application auxiliaire du protocole Internet (IP Helper) décrites dans cette rubrique permettent aux applications en mode utilisateur de déterminer la capacité d’horodatage d’une carte réseau et d’interroger les horodateurs à partir de la carte réseau sous la forme d’horodateurs croisés (décrits ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="492c9-118">In particular, the Internet Protocol Helper (IP Helper) packet timestamping APIs described in this topic provide the ability for user-mode applications to determine the timestamping capability of a network adapter, and to query timestamps from the network adapter in the form of cross timestamps (described below).</span></span>

## <a name="supporting-precision-time-protocol-version-2"></a><span data-ttu-id="492c9-119">Prise en charge du protocole de temps de précision version 2</span><span class="sxs-lookup"><span data-stu-id="492c9-119">Supporting Precision Time Protocol version 2</span></span>

<span data-ttu-id="492c9-120">Comme nous l’avons vu, l’objectif principal de la prise en charge de l’horodatage dans Windows est de prendre en charge le protocole PTPv2 (Precision Time Protocol version 2).</span><span class="sxs-lookup"><span data-stu-id="492c9-120">As mentioned, the main goal of timestamping support in Windows is to support the Precision Time Protocol version 2 (PTPv2) protocol.</span></span> <span data-ttu-id="492c9-121">Dans PTPv2, tous les messages n’ont pas besoin d’un horodatage.</span><span class="sxs-lookup"><span data-stu-id="492c9-121">Within PTPv2, not all messages need a timestamp.</span></span> <span data-ttu-id="492c9-122">En particulier, les messages d’événement PTP utilisent des horodateurs.</span><span class="sxs-lookup"><span data-stu-id="492c9-122">In particular, PTP event messages do use timestamps.</span></span> <span data-ttu-id="492c9-123">Actuellement, la prise en charge est limitée à PTPv2 via le protocole UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="492c9-123">Currently, support is scoped to PTPv2 over User Datagram Protocol (UDP).</span></span> <span data-ttu-id="492c9-124">PTP sur Ethernet brut n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="492c9-124">PTP over raw ethernet isn't supported.</span></span>

<span data-ttu-id="492c9-125">L’horodatage est pris en charge pour les PTPv2 fonctionnant en mode en *2 étapes* .</span><span class="sxs-lookup"><span data-stu-id="492c9-125">Timestamping is supported for PTPv2 operating in *2 step* mode.</span></span> <span data-ttu-id="492c9-126">*2 l’étape* fait référence au mode dans lequel les horodateurs réels dans les paquets PTP ne sont pas générés à la volée dans le matériel, mais sont récupérés à partir du matériel et transmis sous forme de messages distincts (par exemple, à l’aide d’un message de suivi).</span><span class="sxs-lookup"><span data-stu-id="492c9-126">*2 step* refers to the mode in which the actual timestamps in the PTP packets aren't generated on the fly in the hardware, but are instead retrieved from the hardware and conveyed as separate messages (for example, using a follow-up message).</span></span>

<span data-ttu-id="492c9-127">En résumé, vous pouvez utiliser les API d’horodatage des paquets d’assistance IP, ainsi que la prise en charge de l’horodatage de Winsock, dans une application PTPv2 pour améliorer la précision de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="492c9-127">In summary, you can use the Internet Protocol Helper (IP Helper) packet timestamping APIs, together with Winsock's timestamping support, in a PTPv2 application to improve its time synchronization accuracy.</span></span>

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a><span data-ttu-id="492c9-128">Récupération des fonctionnalités d’horodatage d’une carte réseau</span><span class="sxs-lookup"><span data-stu-id="492c9-128">Retrieving the timestamping capabilities of a network adapter</span></span>

<span data-ttu-id="492c9-129">Une application telle qu’un service de synchronisation heure PTP doit déterminer la fonction d’horodatage d’une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="492c9-129">An application such as a PTP time synchronization service needs to determine the timestamping capability of a network adapter.</span></span> <span data-ttu-id="492c9-130">À l’aide des fonctionnalités récupérées, l’application peut ensuite décider s’il souhaite utiliser des horodateurs.</span><span class="sxs-lookup"><span data-stu-id="492c9-130">Using the retrieved capabilities, the application can then decide whether or not it wants to use timestamps.</span></span>

<span data-ttu-id="492c9-131">Même si *une carte réseau prend en* charge les horodateurs, il est nécessaire de conserver la possibilité d’être désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="492c9-131">Even if a network adapter *does* support timestamps, it's required to keep the ability turned off by default.</span></span> <span data-ttu-id="492c9-132">Un adaptateur active l’horodatage lorsqu’il lui est demandé de le faire.</span><span class="sxs-lookup"><span data-stu-id="492c9-132">An adapter turns on timestamping when instructed to do so.</span></span> <span data-ttu-id="492c9-133">Windows fournit des API permettant à une application de récupérer la capacité du matériel, ainsi que les fonctionnalités qui sont activées.</span><span class="sxs-lookup"><span data-stu-id="492c9-133">Windows provides APIs for an application to retrieve the hardware's capability, as well as which capabilities are turned on.</span></span>

<span data-ttu-id="492c9-134">Pour récupérer les fonctionnalités d’horodatage prises en charge d’une carte réseau, vous appelez la fonction [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) , en fournissant l’identificateur unique local (LUID) de la carte réseau et en retournant la récupération des fonctionnalités d’horodatage prises en charge sous la forme d’un objet [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="492c9-134">To retrieve the supported timestamp capabilities of a network adapter, you call the [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the supported timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="492c9-135">Le code retourné par **GetInterfaceSupportedTimestampCapabilities** indique si l’appel a réussi, et si une valeur **INTERFACE_TIMESTAMP_CAPABILITIES** remplie a été récupérée ou non.</span><span class="sxs-lookup"><span data-stu-id="492c9-135">The code returned from **GetInterfaceSupportedTimestampCapabilities** indicates whether or not the call succeeded, and whether or not a populated **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="492c9-136">Pour récupérer les fonctionnalités d’horodatage actuellement activées d’une carte réseau, vous appelez la fonction [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) , en fournissant l’identificateur unique local (LUID) de la carte réseau et en retournant la récupération des fonctionnalités d’horodatage activées sous la forme d’un objet [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="492c9-136">To retrieve the currently enabled timestamp capabilities of a network adapter, you call the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the enabled timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="492c9-137">Là encore, le code retourné par **GetInterfaceActiveTimestampCapabilities** indique la réussite ou l’échec et indique si une valeur **INTERFACE_TIMESTAMP_CAPABILITIES** valide a été récupérée.</span><span class="sxs-lookup"><span data-stu-id="492c9-137">Again, the code returned from **GetInterfaceActiveTimestampCapabilities** indicates success or failure, and whether or not a valid **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="492c9-138">Les cartes réseau peuvent prendre en charge une grande variété de fonctionnalités d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="492c9-138">Network adapters can support a variety of timestamping capabilities.</span></span> <span data-ttu-id="492c9-139">Par exemple, certains adaptateurs peuvent horodater chaque paquet pendant l’envoi et la réception, tandis que d’autres ne prennent en charge que les paquets PTPv2.</span><span class="sxs-lookup"><span data-stu-id="492c9-139">For example, some adapters can timestamp every packet during send and receive, while others support only PTPv2 packets.</span></span> <span data-ttu-id="492c9-140">La structure [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) décrit les fonctionnalités exactes prises en charge par une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="492c9-140">The [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) structure describes the exact capabilities that a network adapter supports.</span></span>

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a><span data-ttu-id="492c9-141">Récupération des horodateurs croisés à partir d’une carte réseau</span><span class="sxs-lookup"><span data-stu-id="492c9-141">Retrieving cross timestamps from a network adapter</span></span>

<span data-ttu-id="492c9-142">Lorsque vous utilisez des horodateurs matériels, une application PTP doit établir une relation (par exemple, en utilisant des techniques mathématiques appropriées) entre l’horloge matérielle de la carte réseau et une horloge système.</span><span class="sxs-lookup"><span data-stu-id="492c9-142">When using hardware timestamps, a PTP application needs to establish a relation (for example, by using appropriate mathematical techniques) between the hardware clock of the network adapter and a system clock.</span></span> <span data-ttu-id="492c9-143">Cela est nécessaire pour qu’une valeur représentant une heure dans l’unité d’une horloge puisse être convertie en unité d’une autre horloge.</span><span class="sxs-lookup"><span data-stu-id="492c9-143">This is necessary so that a value representing a time in one clock's unit can be converted into another clock's unit.</span></span> <span data-ttu-id="492c9-144">Les horodateurs croisés sont fournis à cet effet, et votre application peut périodiquement échantillonner les horodateurs croisés afin d’établir une telle relation.</span><span class="sxs-lookup"><span data-stu-id="492c9-144">Cross timestamps are provided for this purpose, and your application can sample cross timestamps periodically in order to establish such a relation.</span></span>

<span data-ttu-id="492c9-145">Pour ce faire, appelez la fonction [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) , en fournissant l’identificateur unique local (LUID) de la carte réseau et en retournant la récupération de l’horodateur à partir de la carte réseau sous la forme d’un objet [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) .</span><span class="sxs-lookup"><span data-stu-id="492c9-145">To do that, call the [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the timestamp from the network adapter in the form of an [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) object.</span></span>

## <a name="timestamp-capability-change-notifications"></a><span data-ttu-id="492c9-146">Notifications de modification de la capacité d’horodatage</span><span class="sxs-lookup"><span data-stu-id="492c9-146">Timestamp capability change notifications</span></span>

<span data-ttu-id="492c9-147">Pour être notifié, les fonctionnalités d’horodatage pour une carte réseau changent. appelez la fonction [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) , en fournissant un pointeur vers la fonction de rappel que vous avez implémentée, ainsi qu’un contexte facultatif alloué par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="492c9-147">To be notified should the timestamp capabilities for a network adapter change, call the [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) function, providing a pointer to the callback function that you've implemented, together with an optional caller-allocated context.</span></span>

<span data-ttu-id="492c9-148">**RegisterInterfaceTimestampConfigChange** retourne un handle que vous pouvez ensuite passer à [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) pour annuler l’inscription de votre fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="492c9-148">**RegisterInterfaceTimestampConfigChange** returns a handle that you can subsequently pass to [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) in order to unregister your callback function.</span></span>

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a><span data-ttu-id="492c9-149">Exemple de code 1 &mdash; récupération des fonctionnalités d’horodatage et des horodateurs croisés</span><span class="sxs-lookup"><span data-stu-id="492c9-149">Code example 1&mdash;retrieving timestamp capabilities and cross timestamps</span></span>

```c
// main.cpp in a Console App project.

#include <stdio.h>
#include <winsock2.h>
#include <iphlpapi.h>
#pragma comment(lib, "Iphlpapi")

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv4(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv6(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// This function checks and returns the supported timestamp capabilities for an interface for
// a PTPv2 application
SupportedTimestampType
CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities;
    SupportedTimestampType supportedType = TimestampTypeNone;

    result = GetInterfaceActiveTimestampCapabilities(
                 &interfaceLuid,
                 &timestampCapabilities);
    if (result != NO_ERROR)
    {
        printf("Error retrieving hardware timestamp capabilities: %d\n", result);
        goto Exit;
    }

    if (IsPTPv2HardwareTimestampingSupportedForIPv4(&timestampCapabilities) &&
        IsPTPv2HardwareTimestampingSupportedForIPv6(&timestampCapabilities))
    {
        supportedType = TimestampTypeHardware;
        goto Exit;
    }
    else
    {
        if ((timestampCapabilities.SoftwareCapabilities.AllReceive) &&
            ((timestampCapabilities.SoftwareCapabilities.AllTransmit) ||
             (timestampCapabilities.SoftwareCapabilities.TaggedTransmit)))
        {
            supportedType = TimestampTypeSoftware;
        }
    }

Exit:
    return supportedType;
}

// Helper function which does the correlation between hardware and system clock
// using mathematical techniques
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// An application would call this function periodically to gather a set 
// of matching timestamps for use in converting hardware timestamps to
// system timestamps
DWORD
RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp;

    result = CaptureInterfaceHardwareCrossTimestamp(
                 &interfaceLuid,
                 &crossTimestamp);
    if (result != NO_ERROR)
    {
        printf("Error retrieving cross timestamp for the interface: %d\n", result);
        goto Exit;
    }

    // Process crossTimestamp further to create a relation between the hardware clock
    // of the NIC and the QPC values using appropriate mathematical techniques
    ComputeCorrelationOfHardwareAndSystemTimestamps(&crossTimestamp);

Exit:
    return result;
}

int main()
{
}
```

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a><span data-ttu-id="492c9-150">Exemple de code 2 &mdash; inscription pour les notifications de modification de capacité d’horodatage</span><span class="sxs-lookup"><span data-stu-id="492c9-150">Code example 2&mdash;registering for timestamp capability change notifications</span></span>

<span data-ttu-id="492c9-151">Cet exemple montre comment votre application peut utiliser des horodateurs de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="492c9-151">This example shows how your application could use timestamps end to end.</span></span>

```c
// main.cpp in a Console App project.

#include <stdlib.h>
#include <stdio.h>
#include <winsock2.h>
#include <mswsock.h>
#include <iphlpapi.h>
#include <mstcpip.h>
#pragma comment(lib, "Ws2_32")
#pragma comment(lib, "Iphlpapi")

// Globals and function declarations used by the application.
// The sample functions and skeletons demonstrate:
// - Checking timestamp configuration for an interface to determine if timestamping can be used
// - If timestamping is enabled, starts tracking changes in timestamp configuration
// - Performing correlation between hardware and system timestamps using cross timestamps
//   on a separate thread depending on the timestamp type configured
// - Receiving a packet and computing the latency between when the timestamp
//   was generated on packet reception, and when the packet was received by
//   the application through the socket
// The sample tries to demonstrate how an application could use timestamps. It is not thread safe 
// and does not do exhaustive error checking.
// Lot of the functions are provided as skeletons, or only declared and invoked
// but are not defined. It is up to
// the application to implement these suitably.

// An application could use the functions below by e.g.
// - Call InitializeTimestampingForInterface for the interface it wants to track for timestamping capability.
// - Call EstimateReceiveLatency to estimate the receive latency of a packet depending on the timestamp 
//   type configured for the interface.

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// interfaceBeingTracked is the interface the PTPv2 application
// intends to use for timestamping purpose.
wchar_t* interfaceBeingTracked;

// The active timestamping type determined for
// interfaceBeingTracked.
SupportedTimestampType timestampTypeEnabledForInterface;

HANDLE correlationThread;
HANDLE threadStopEvent;
HIFTIMESTAMPCHANGE TimestampChangeNotificationHandle = NULL;

// Function from sample above to check if an interface supports timestamping for PTPv2.
SupportedTimestampType CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid);

// Function from sample above to retrieve cross timestamps and process them further.
DWORD RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid);

// Helper function which registers for timestamp configuration changes.
DWORD RegisterTimestampChangeNotifications();

// Callback function which is invoked when timestamp configuration changes
// for some network interface.
INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK TimestampConfigChangeCallback;

// Function which does the correlation between hardware and system clock
// using mathematical techniques. It is periodically invoked and provided
// a sample of cross timestamp to compute a correlation.
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// Helper function which converts a hardware timestamp from the NIC clock
// to system timestamp (QPC) values. It is assumed that this works together
// with the ComputeCorrelationOfHardwareAndSystemTimestamps function
// to derive the correlation.
ULONG64 ConvertHardwareTimestampToQpc(ULONG64 HardwareTimestamp);

// Start function of thread which periodically samples
// cross timestamps to correlate hardware and software timestamps.
DWORD WINAPI CorrelateHardwareAndSystemTimestamps(LPVOID);

// Helper function which starts a new thread at CorrelateHardwareAndSystemTimestamps.
DWORD StartCorrelatingHardwareAndSytemTimestamps();

// Helper function which restarts correlation when some change is detected.
DWORD RestartCorrelatingHardwareAndSystemTimestamps();

// Stops the correlation thread.
DWORD StopCorrelatingHardwareAndSystemTimestamps();

DWORD
FindInterfaceFromFriendlyName(wchar_t* friendlyName, NET_LUID* interfaceLuid)
{
    DWORD result = 0;
    ULONG flags = 0;
    ULONG outBufLen = 0;
    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    PIP_ADAPTER_ADDRESSES currentAddresses = NULL;

    result = GetAdaptersAddresses(0,
        flags,
        NULL,
        pAddresses,
        &outBufLen);
    if (result == ERROR_BUFFER_OVERFLOW)
    {
        pAddresses = (PIP_ADAPTER_ADDRESSES)malloc(outBufLen);

        result = GetAdaptersAddresses(0,
            flags,
            NULL,
            pAddresses,
            &outBufLen);
        if (result != NO_ERROR)
        {
            goto Done;
        }
    }
    else if (result != NO_ERROR)
    {
        goto Done;
    }

    currentAddresses = pAddresses;
    while (currentAddresses != NULL)
    {
        if (wcscmp(friendlyName, currentAddresses->FriendlyName) == 0)
        {
            result = ConvertInterfaceIndexToLuid(currentAddresses->IfIndex, interfaceLuid);
            goto Done;
        }

        currentAddresses = currentAddresses->Next;
    }

    result = ERROR_NOT_FOUND;

Done:

    if (pAddresses != NULL)
    {
        free(pAddresses);
    }

    return result;
}

// This function checks if an interface is suitable for
// timestamping for PTPv2. If so, it registers for timestamp
// configuration changes and initializes some globals.
// If hardware  timestamping is enabled it also starts
// correlation thread.
DWORD
InitializeTimestampingForInterface(wchar_t* friendlyName)
{
    DWORD error;
    SupportedTimestampType supportedType = TimestampTypeNone;

    NET_LUID interfaceLuid;

    error = FindInterfaceFromFriendlyName(friendlyName, &interfaceLuid);
    if (error != 0)
    {
        return error;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if (supportedType != TimestampTypeNone)
    {
        error = RegisterTimestampChangeNotifications();
        if (error != NO_ERROR)
        {
            return error;
        }

        if (supportedType == TimestampTypeHardware)
        {
            threadStopEvent = CreateEvent(
                NULL,
                FALSE,
                FALSE,
                NULL
            );
            if (threadStopEvent == NULL)
            {
                return GetLastError();
            }            

            error = StartCorrelatingHardwareAndSytemTimestamps();
            if (error != 0)
            {
                return error;
            }
        }

        interfaceBeingTracked = friendlyName;
        timestampTypeEnabledForInterface = supportedType;

        return error;
    }

    return ERROR_NOT_SUPPORTED;
}

DWORD
RegisterTimestampChangeNotifications()
{
    DWORD retcode = NO_ERROR;

    // Register with NULL context
    retcode = RegisterInterfaceTimestampConfigChange(TimestampConfigChangeCallback, NULL, &TimestampChangeNotificationHandle);
    if (retcode != NO_ERROR)
    {
        printf("Error when calling RegisterIfTimestampConfigChange %d\n", retcode);
    }

    return retcode;
}

// The callback invoked when change in some interface’s timestamping configuration
// happens. The callback takes appropriate action based on the new capability of the
// interface. The callback assumes that there is only 1 NIC. If multiple NICs are being
// tracked for timestamping then the application would need to check all of them.
VOID
WINAPI
TimestampConfigChangeCallback(
    _In_ PVOID /*CallerContext*/
    )
{
    SupportedTimestampType supportedType;

    NET_LUID interfaceLuid;
    DWORD error;

    error = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (error != NO_ERROR)
    {
        if (timestampTypeEnabledForInterface == TimestampTypeHardware)
        {
            StopCorrelatingHardwareAndSystemTimestamps();
            timestampTypeEnabledForInterface = TimestampTypeNone;
        }
        return;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if ((supportedType == TimestampTypeHardware) &&
        (timestampTypeEnabledForInterface == TimestampTypeHardware))
    {
        // NIC could have been restarted, restart the correlation between hardware and 
        // system timestamps.
        RestartCorrelatingHardwareAndSystemTimestamps();
    }
    else if (supportedType == TimestampTypeHardware)
    {
        // Start thread correlating hardware and software timestamps
        StartCorrelatingHardwareAndSytemTimestamps();
    }
    else if (supportedType != TimestampTypeHardware)
    {
        // Hardware timestamps are not enabled, stop correlation
        StopCorrelatingHardwareAndSystemTimestamps();
    }

    timestampTypeEnabledForInterface = supportedType;
}

DWORD 
StartCorrelatingHardwareAndSytemTimestamps()
{
    // Create a new thread which starts at CorrelateHardwareAndSoftwareTimestamps
    correlationThread = CreateThread(
        NULL,
        0,
        CorrelateHardwareAndSystemTimestamps,
        NULL,
        0,
        NULL); 

    if (correlationThread == NULL)
    {
        return GetLastError();
    }
}

// Thread which periodically invokes functions to 
// sample cross timestamps and use them to compute
// correlation between hardware and system timestamps.
DWORD WINAPI
CorrelateHardwareAndSystemTimestamps(LPVOID /*lpParameter*/)
{
    DWORD error;
    NET_LUID interfaceLuid;
    DWORD result;

    result = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (result != 0)
    {
        return result;
    }

    while (TRUE)
    {
        error = RetrieveAndProcessCrossTimestamp(interfaceLuid);

        // Sleep and repeat till the thread gets a signal to stop
        result = WaitForSingleObject(threadStopEvent, 5000);
        if (result != WAIT_TIMEOUT)
        {
            if (result == WAIT_OBJECT_0)
            {
                return 0;
            }
            else if (result == WAIT_FAILED)            
            {
                return GetLastError();
            }

            return result;
        }
    }
}

DWORD
StopCorrelatingHardwareAndSystemTimestamps()
{
    SetEvent(threadStopEvent);
    return 0;
}

// Function which receives a packet and estimates the latency between the 
// point at which receive timestamp (of appropriate type) was generated
// and when the packet was received in the app through the socket.
// The sample assumes that there is only 1 NIC in the system. This is the NIC which is tracked through
// interfaceBeingTracked for correlation purpose, and through which packets are being
// received by the socket.
// The recvmsg parameter is of type LPFN_WSARECVMSG and an application can
// retrieve it by issuing WSAIoctl
// with SIO_GET_EXTENSION_FUNCTION_POINTER control
// and WSAID_WSARECVMSG. Please refer to msdn.
void EstimateReceiveLatency(SOCKET sock, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;
    ULONG64 packetReceivedTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.Flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    if (timestampTypeEnabledForInterface != TimestampTypeNone)
    {
        // Capture system timestamp (QPC) upon message reception.
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;

        printf("received packet\n");

        // Look for socket rx timestamp returned via control message.
        BOOLEAN retrievedTimestamp = FALSE;
        PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
        while (cmsg != NULL)
        {
            if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP)
            {
                socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
                retrievedTimestamp = TRUE;
                break;
            }
            cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
        }

        if (retrievedTimestamp)
        {
            // Compute socket receive path latency.
            LARGE_INTEGER clockFrequency;
            ULONG64 elapsedMicroseconds;

            if (timestampTypeEnabledForInterface == TimestampTypeHardware)
            {
                packetReceivedTimestamp = ConvertHardwareTimestampToQpc(socketTimestamp);
            }
            else
            {
                packetReceivedTimestamp = socketTimestamp;
            }
        
            QueryPerformanceFrequency(&clockFrequency);

            // Compute socket receive path latency.
            elapsedMicroseconds = appLevelTimestamp - packetReceivedTimestamp;
            elapsedMicroseconds *= 1000000;
            elapsedMicroseconds /= clockFrequency.QuadPart;
            printf("RX latency estimation: %lld microseconds\n",
                 elapsedMicroseconds);
        }
        else
        {
            printf("failed to retrieve RX timestamp\n");
        }
    }
}

int main()
{
}
```

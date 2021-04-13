---
description: L’assistance IP fournit des fonctionnalités pour la gestion des cartes réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gestion des cartes réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525893"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="358fd-105">Gestion des cartes réseau</span><span class="sxs-lookup"><span data-stu-id="358fd-105">Managing Network Adapters</span></span>

<span data-ttu-id="358fd-106">L’assistance IP fournit des fonctionnalités pour la gestion des cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="358fd-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="358fd-107">Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="358fd-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="358fd-108">Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.</span><span class="sxs-lookup"><span data-stu-id="358fd-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="358fd-109">Utilisez les fonctions décrites dans les paragraphes suivants pour récupérer des informations sur les cartes réseau de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="358fd-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="358fd-110">La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retourne un tableau de structures d' [**\_ \_ informations de cartes IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , une pour chaque carte de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="358fd-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="358fd-111">La fonction [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) retourne des informations supplémentaires sur un adaptateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="358fd-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="358fd-112">La fonction **GetPerAdapterInfo** oblige l’appelant à spécifier l’index de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="358fd-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="358fd-113">Pour obtenir l’index de l’adaptateur à partir du nom de l’adaptateur, utilisez la fonction [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .</span><span class="sxs-lookup"><span data-stu-id="358fd-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="358fd-114">Certaines applications utilisent des adaptateurs qui reçoivent des datagrammes, mais ne peuvent pas les transmettre.</span><span class="sxs-lookup"><span data-stu-id="358fd-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="358fd-115">Pour obtenir des informations sur ces adaptateurs, utilisez la fonction [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .</span><span class="sxs-lookup"><span data-stu-id="358fd-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="358fd-116">La fonction [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) vous permet de récupérer les adresses IP associées à un adaptateur particulier.</span><span class="sxs-lookup"><span data-stu-id="358fd-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="358fd-117">Cette fonction prend en charge l’adressage IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="358fd-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="358fd-118">Pour obtenir des exemples de code impliquant des [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consultez [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="358fd-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 




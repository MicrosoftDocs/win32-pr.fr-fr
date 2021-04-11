---
description: L’assistance IP étend vos capacités de gestion des interfaces réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gestion des interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202757"
---
# <a name="managing-interfaces"></a><span data-ttu-id="d1417-105">Gestion des interfaces</span><span class="sxs-lookup"><span data-stu-id="d1417-105">Managing Interfaces</span></span>

<span data-ttu-id="d1417-106">L’assistance IP étend vos capacités de gestion des interfaces réseau.</span><span class="sxs-lookup"><span data-stu-id="d1417-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="d1417-107">Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="d1417-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="d1417-108">Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.</span><span class="sxs-lookup"><span data-stu-id="d1417-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="d1417-109">Utilisez les fonctions décrites dans les paragraphes suivants pour gérer les interfaces sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1417-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="d1417-110">La fonction [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) retourne le nombre d’interfaces sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1417-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="d1417-111">La fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) retourne une table qui contient les noms et les index correspondants pour les interfaces sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1417-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="d1417-112">Pour obtenir des exemples de code impliquant des **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="d1417-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="d1417-113">La fonction [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) prend un index d’interface et retourne un index d’interface à compatibilité descendante, c’est-à-dire un index qui utilise uniquement les 24 bits inférieurs.</span><span class="sxs-lookup"><span data-stu-id="d1417-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="d1417-114">Ce type d’index est parfois appelé index d’interface « convivial ».</span><span class="sxs-lookup"><span data-stu-id="d1417-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="d1417-115">La fonction [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) retourne une structure [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) qui contient des informations sur une interface particulière sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1417-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="d1417-116">Cette fonction requiert que l’appelant fournisse l’index de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d1417-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="d1417-117">La fonction [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) retourne une table d' [**entrées \_ IFROW MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , une pour chaque interface sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d1417-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="d1417-118">Utilisez la fonction [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) pour modifier la configuration d’une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="d1417-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 

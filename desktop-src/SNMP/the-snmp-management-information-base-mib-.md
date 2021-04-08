---
title: Base de données MIB (Management Information base) SNMP
description: Une base d’informations de gestion (MIB) décrit un ensemble d’objets gérés. Une application de console de gestion SNMP peut manipuler les objets sur un ordinateur spécifique si le service SNMP a une DLL d’agent d’extension qui prend en charge la MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672085"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="baa14-104">Base de données MIB (Management Information base) SNMP</span><span class="sxs-lookup"><span data-stu-id="baa14-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="baa14-105">Une base d’informations de gestion (MIB) décrit un ensemble d’objets gérés.</span><span class="sxs-lookup"><span data-stu-id="baa14-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="baa14-106">Une application de console de gestion SNMP peut manipuler les objets sur un ordinateur spécifique si le service SNMP a une DLL d’agent d’extension qui prend en charge la MIB.</span><span class="sxs-lookup"><span data-stu-id="baa14-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="baa14-107">Chaque objet géré dans un MIB a un identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="baa14-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="baa14-108">L’identificateur comprend le type de l’objet (par exemple, compteur, chaîne, jauge ou adresse), le niveau d’accès de l’objet (par exemple, lecture ou lecture/écriture), les restrictions de taille et les informations de plage.</span><span class="sxs-lookup"><span data-stu-id="baa14-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="baa14-109">Le tableau suivant contient une liste partielle des MIB fournis avec le système.</span><span class="sxs-lookup"><span data-stu-id="baa14-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="baa14-110">Ils sont installés avec le service SNMP dans le répertoire% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="baa14-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="baa14-111">Pour obtenir la liste complète des MIB, reportez-vous au kit de ressources Windows.</span><span class="sxs-lookup"><span data-stu-id="baa14-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="baa14-112">MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-112">MIB</span></span>         | <span data-ttu-id="baa14-113">Description</span><span class="sxs-lookup"><span data-stu-id="baa14-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa14-114">DHCP. MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-114">DHCP.MIB</span></span>    | <span data-ttu-id="baa14-115">La MIB définie par Microsoft qui contient des types d’objet pour analyser le trafic réseau entre les hôtes distants et les serveurs DHCP</span><span class="sxs-lookup"><span data-stu-id="baa14-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="baa14-116">HOSTMIB. MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="baa14-117">Contient les types d’objets pour l’analyse et la gestion des ressources hôtes</span><span class="sxs-lookup"><span data-stu-id="baa14-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="baa14-118">LMMIB2. MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="baa14-119">Couvre les services de station de travail et de serveur</span><span class="sxs-lookup"><span data-stu-id="baa14-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="baa14-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-120">MIB\_II.MIB</span></span> | <span data-ttu-id="baa14-121">Contient la base d’informations de gestion (MIB-II), qui fournit une architecture et un système simples et réalisables pour la gestion des adresses Internet TCP/IP</span><span class="sxs-lookup"><span data-stu-id="baa14-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="baa14-122">WINS. MIB</span><span class="sxs-lookup"><span data-stu-id="baa14-122">WINS.MIB</span></span>    | <span data-ttu-id="baa14-123">La MIB définie par Microsoft pour le service WINS (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="baa14-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="baa14-124">**Windows NT :** En règle générale, vous pouvez copier une MIB à partir de l’agent d’extension SNMP qui prend en charge la MIB particulière.</span><span class="sxs-lookup"><span data-stu-id="baa14-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="baa14-125">Des MIB supplémentaires sont disponibles avec le kit de ressources Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="baa14-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="baa14-126">Les dll de l’agent d’extension pour MIB-II, LAN Manager MIB-II et la MIB des ressources de l’ordinateur hôte sont installées avec le service SNMP.</span><span class="sxs-lookup"><span data-stu-id="baa14-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="baa14-127">Les dll de l’agent d’extension pour les autres MIB sont installées lors de l’installation de leurs services respectifs.</span><span class="sxs-lookup"><span data-stu-id="baa14-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="baa14-128">Au moment du démarrage du service, le service SNMP charge toutes les dll de l’agent d’extension répertoriées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="baa14-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="baa14-129">Les utilisateurs peuvent ajouter d’autres DLL d’agent d’extension qui implémentent des MIB supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="baa14-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="baa14-130">Pour ce faire, ils doivent ajouter une entrée de Registre pour la nouvelle DLL sous le service SNMP.</span><span class="sxs-lookup"><span data-stu-id="baa14-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="baa14-131">Ils doivent également inscrire la nouvelle MIB auprès de l’application de la console de gestion SNMP.</span><span class="sxs-lookup"><span data-stu-id="baa14-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="baa14-132">Pour plus d’informations, consultez la documentation fournie avec votre application console de gestion.</span><span class="sxs-lookup"><span data-stu-id="baa14-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="baa14-133">Pour plus d’informations, consultez [MIB Name Tree](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="baa14-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 





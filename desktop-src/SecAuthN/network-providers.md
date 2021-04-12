---
description: Un fournisseur de réseau est une DLL qui prend en charge un protocole réseau spécifique.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Fournisseurs de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204156"
---
# <a name="network-providers"></a><span data-ttu-id="3d8dc-103">Fournisseurs de réseau</span><span class="sxs-lookup"><span data-stu-id="3d8dc-103">Network Providers</span></span>

<span data-ttu-id="3d8dc-104">Un fournisseur de réseau est une DLL qui prend en charge un protocole réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="3d8dc-105">Il implémente également l' [API du fournisseur réseau](network-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="3d8dc-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="3d8dc-106">Cela lui permet d’interagir avec le système d’exploitation Windows pour recevoir les demandes réseau standard, telles que les demandes de connexion ou de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="3d8dc-107">Pour gérer ces requêtes, le fournisseur réseau appelle ensuite l’API spécifique au réseau qui est appropriée au protocole réseau pris en charge par le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="3d8dc-108">En d’autres termes, le fournisseur réseau encapsule les fonctionnalités spécifiques au réseau dans une DLL, qui expose une interface standard à Windows.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="3d8dc-109">Grâce aux fournisseurs de réseau, Windows peut prendre en charge de nombreux types de protocoles réseau sans avoir à connaître les détails spécifiques au réseau de chaque réseau.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="3d8dc-110">Cela est essentiel, car les nouveaux protocoles réseau sont en cours de développement en permanence.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="3d8dc-111">Avec les fournisseurs de réseau, la prise en charge d’un nouveau protocole nécessite simplement la création et l’installation d’un nouveau fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="3d8dc-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="3d8dc-112">Pour plus d’informations sur les structures et les fonctions des fournisseurs de réseau, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d8dc-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="3d8dc-113">Fonctions du fournisseur de réseau</span><span class="sxs-lookup"><span data-stu-id="3d8dc-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="3d8dc-114">Structures de fournisseur réseau</span><span class="sxs-lookup"><span data-stu-id="3d8dc-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 




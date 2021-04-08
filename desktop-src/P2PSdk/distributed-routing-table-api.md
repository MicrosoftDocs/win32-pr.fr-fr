---
description: L’API DRT (Distributed Routing Table) permet aux applications de publier et de résoudre des clés numériques sur un réseau pair à pair.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API Table de routage distribué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034521"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="5e965-103">API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="5e965-103">Distributed Routing Table API</span></span>

<span data-ttu-id="5e965-104">L’API DRT (Distributed Routing Table) permet aux applications de publier et de résoudre des clés numériques sur un réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="5e965-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="5e965-105">Une application utilisant DRT peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e965-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="5e965-106">Créer des tables de routage distribuées spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="5e965-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="5e965-107">Enregistrez les clés et associez ces clés aux adresses IP et aux données d’application.</span><span class="sxs-lookup"><span data-stu-id="5e965-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="5e965-108">Recherchez les clés et récupérez les adresses IP et les données d’application qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="5e965-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="5e965-109">Cette fonctionnalité peut être utilisée pour construire des tables de hachage distribuée (DHTs), des systèmes de résolution de noms sans serveur et des réseaux de maillage de superposition de nombreuses topologies.</span><span class="sxs-lookup"><span data-stu-id="5e965-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="5e965-110">Les administrateurs et les utilisateurs des applications compatibles DRT doivent rendre les utilisateurs finaux de leurs applications informés des informations publiées.</span><span class="sxs-lookup"><span data-stu-id="5e965-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="5e965-111">Les serveurs Microsoft ne sont pas utilisés par cette technologie et les informations ne sont pas envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5e965-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="5e965-112">La documentation fournie pour cette API est divisée en trois sections.</span><span class="sxs-lookup"><span data-stu-id="5e965-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="5e965-113">Section</span><span class="sxs-lookup"><span data-stu-id="5e965-113">Section</span></span>                                                                                | <span data-ttu-id="5e965-114">Description</span><span class="sxs-lookup"><span data-stu-id="5e965-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e965-115">À propos des tables de routage distribuées</span><span class="sxs-lookup"><span data-stu-id="5e965-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="5e965-116">Informations détaillant le cycle de vie et les changements d’état de l’API DRT.</span><span class="sxs-lookup"><span data-stu-id="5e965-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="5e965-117">Utilisation du API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="5e965-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="5e965-118">Informations détaillant l’utilisation générale de l’API DRT.</span><span class="sxs-lookup"><span data-stu-id="5e965-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="5e965-119">Référence de API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="5e965-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="5e965-120">Informations détaillant les fonctions, les structures de données et les constantes énumérées qui composent l’API DRT.</span><span class="sxs-lookup"><span data-stu-id="5e965-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 





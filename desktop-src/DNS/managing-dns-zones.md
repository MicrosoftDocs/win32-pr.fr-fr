---
title: Gestion des Zones DNS
description: Une zone DNS est une base de données d’entrées RR qui correspond à une partie de l’espace de noms hiérarchique DNS. Les zones DNS servent à découper les serveurs DNS faisant autorité pour la résolution des requêtes de résolution de noms pour une section donnée de la hiérarchie DNS.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674482"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="a8cd6-104">Gestion des Zones DNS</span><span class="sxs-lookup"><span data-stu-id="a8cd6-104">Managing DNS Zones</span></span>

<span data-ttu-id="a8cd6-105">Une zone DNS est une base de données d’entrées RR qui correspond à une partie de l’espace de noms hiérarchique DNS.</span><span class="sxs-lookup"><span data-stu-id="a8cd6-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="a8cd6-106">Les zones DNS servent à découper les serveurs DNS faisant autorité pour la résolution des requêtes de résolution de noms pour une section donnée de la hiérarchie DNS.</span><span class="sxs-lookup"><span data-stu-id="a8cd6-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="a8cd6-107">Étapes d’administration</span><span class="sxs-lookup"><span data-stu-id="a8cd6-107">Administration Steps</span></span>

<span data-ttu-id="a8cd6-108">Le fournisseur WMI DNS permet d’administrer des zones DNS à partir du serveur DNS faisant autorité, ou à partir d’hôtes distants.</span><span class="sxs-lookup"><span data-stu-id="a8cd6-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="a8cd6-109">Les étapes générales nécessaires à l’administration d’une zone à l’aide du fournisseur WMI DNS sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8cd6-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="a8cd6-110">Connexion au fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="a8cd6-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="a8cd6-111">Obtention d’une instance de zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-111">Getting a zone instance</span></span>
-   <span data-ttu-id="a8cd6-112">Énumération ou modification d’une propriété de zone, ou utilisation d’une méthode</span><span class="sxs-lookup"><span data-stu-id="a8cd6-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="a8cd6-113">Les tâches suivantes sont liées aux exemples de scripts associés :</span><span class="sxs-lookup"><span data-stu-id="a8cd6-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="a8cd6-114">Création d’une zone DNS</span><span class="sxs-lookup"><span data-stu-id="a8cd6-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-115">Modification d’une zone DNS</span><span class="sxs-lookup"><span data-stu-id="a8cd6-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-116">Suppression d’une zone DNS</span><span class="sxs-lookup"><span data-stu-id="a8cd6-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-117">Ajout d’une adresse IP de zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-118">Suppression d’une adresse IP de zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-119">Suspension d’une zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-120">Reprise d’une zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-121">Mise à jour d’une zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-122">Rechargement d’une zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="a8cd6-123">Actualisation d’une zone</span><span class="sxs-lookup"><span data-stu-id="a8cd6-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 





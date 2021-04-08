---
title: Gestion des serveurs DNS
description: Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674485"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="1fc07-103">Gestion des serveurs DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-103">Managing DNS Servers</span></span>

<span data-ttu-id="1fc07-104">Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.</span><span class="sxs-lookup"><span data-stu-id="1fc07-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="1fc07-105">Les serveurs DNS contiennent des fichiers, appelés *fichiers de zone*, qui leur permettent de résoudre les noms en adresses IP (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="1fc07-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="1fc07-106">Lorsqu’il est interrogé, un serveur DNS répond de l’une des trois façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fc07-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="1fc07-107">Le serveur renvoie les informations de résolution de noms ou de résolution IP demandées.</span><span class="sxs-lookup"><span data-stu-id="1fc07-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="1fc07-108">Le serveur retourne un pointeur vers un autre serveur DNS qui peut traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="1fc07-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="1fc07-109">Le serveur indique qu’il ne dispose pas des informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1fc07-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="1fc07-110">Les serveurs DNS peuvent, au cours de la préparation, retourner les informations de résolution demandées, interroger d’autres serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="1fc07-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="1fc07-111">Mais au-delà de cela, les serveurs DNS n’effectuent aucune opération autre que celles mentionnées dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="1fc07-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="1fc07-112">Il existe trois types principaux de serveurs DNS : les serveurs principaux, les serveurs secondaires et les serveurs de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="1fc07-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="1fc07-113">Pour plus d’informations sur ces serveurs DNS, consultez [serveurs DNS](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc07-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="1fc07-114">Étapes d’administration</span><span class="sxs-lookup"><span data-stu-id="1fc07-114">Administration Steps</span></span>

<span data-ttu-id="1fc07-115">Le fournisseur WMI DNS permet l’administration de serveurs DNS à partir du serveur lui-même ou à partir d’hôtes distants.</span><span class="sxs-lookup"><span data-stu-id="1fc07-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="1fc07-116">Les étapes générales nécessaires à l’administration d’un serveur DNS à l’aide du fournisseur WMI DNS sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fc07-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="1fc07-117">Connexion au fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="1fc07-118">Obtention d’une instance de serveur</span><span class="sxs-lookup"><span data-stu-id="1fc07-118">Getting a server instance</span></span>
-   <span data-ttu-id="1fc07-119">Énumération ou modification d’une propriété de serveur, ou utilisation d’une méthode</span><span class="sxs-lookup"><span data-stu-id="1fc07-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="1fc07-120">Pour illustrer comment implémenter ces étapes d’administration, des exemples sont fournis.</span><span class="sxs-lookup"><span data-stu-id="1fc07-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="1fc07-121">Les tâches suivantes sont liées aux exemples de script associés.</span><span class="sxs-lookup"><span data-stu-id="1fc07-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="1fc07-122">Arrêt d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-123">Démarrage d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-124">Redémarrage d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-125">Ajout d’une adresse IP</span><span class="sxs-lookup"><span data-stu-id="1fc07-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-126">Suppression d’une adresse IP</span><span class="sxs-lookup"><span data-stu-id="1fc07-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-127">Liste des propriétés du serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-128">Affichage des types de propriété de serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1fc07-129">Modification des propriétés d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1fc07-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 





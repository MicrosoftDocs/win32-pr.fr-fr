---
title: Gestion des serveurs DNS
description: En savoir plus sur la gestion des serveurs DNS. Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010772"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="1d0ff-104">Gestion des serveurs DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-104">Managing DNS Servers</span></span>

<span data-ttu-id="1d0ff-105">Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="1d0ff-106">Les serveurs DNS contiennent des fichiers, appelés *fichiers de zone*, qui leur permettent de résoudre les noms en adresses IP (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="1d0ff-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="1d0ff-107">Lorsqu’il est interrogé, un serveur DNS répond de l’une des trois façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d0ff-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="1d0ff-108">Le serveur renvoie les informations de résolution de noms ou de résolution IP demandées.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="1d0ff-109">Le serveur retourne un pointeur vers un autre serveur DNS qui peut traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="1d0ff-110">Le serveur indique qu’il ne dispose pas des informations demandées.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="1d0ff-111">Les serveurs DNS peuvent, au cours de la préparation, retourner les informations de résolution demandées, interroger d’autres serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="1d0ff-112">Mais au-delà de cela, les serveurs DNS n’effectuent aucune opération autre que celles mentionnées dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="1d0ff-113">Il existe trois types principaux de serveurs DNS : les serveurs principaux, les serveurs secondaires et les serveurs de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="1d0ff-114">Pour plus d’informations sur ces serveurs DNS, consultez [serveurs DNS](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="1d0ff-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="1d0ff-115">Étapes d’administration</span><span class="sxs-lookup"><span data-stu-id="1d0ff-115">Administration Steps</span></span>

<span data-ttu-id="1d0ff-116">Le fournisseur WMI DNS permet l’administration de serveurs DNS à partir du serveur lui-même ou à partir d’hôtes distants.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="1d0ff-117">Les étapes générales nécessaires à l’administration d’un serveur DNS à l’aide du fournisseur WMI DNS sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d0ff-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="1d0ff-118">Connexion au fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="1d0ff-119">Obtention d’une instance de serveur</span><span class="sxs-lookup"><span data-stu-id="1d0ff-119">Getting a server instance</span></span>
-   <span data-ttu-id="1d0ff-120">Énumération ou modification d’une propriété de serveur, ou utilisation d’une méthode</span><span class="sxs-lookup"><span data-stu-id="1d0ff-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="1d0ff-121">Pour illustrer comment implémenter ces étapes d’administration, des exemples sont fournis.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="1d0ff-122">Les tâches suivantes sont liées aux exemples de script associés.</span><span class="sxs-lookup"><span data-stu-id="1d0ff-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="1d0ff-123">Arrêt d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-124">Démarrage d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-125">Redémarrage d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-126">Ajout d’une adresse IP</span><span class="sxs-lookup"><span data-stu-id="1d0ff-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-127">Suppression d’une adresse IP</span><span class="sxs-lookup"><span data-stu-id="1d0ff-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-128">Liste des propriétés du serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-129">Affichage des types de propriété de serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="1d0ff-130">Modification des propriétés d’un serveur DNS</span><span class="sxs-lookup"><span data-stu-id="1d0ff-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 





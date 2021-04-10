---
title: Vue d’ensemble du fournisseur WMI DNS
description: Un fournisseur est un élément architectural de Windows Management Instrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, fournisseur WMI, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029081"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="66744-104">Vue d’ensemble du fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="66744-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="66744-105">Un fournisseur est un élément architectural de *Windows Management Instrumentation (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="66744-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="66744-106">WMI définit une architecture unifiée pour décrire, accéder et instrumenter des objets.</span><span class="sxs-lookup"><span data-stu-id="66744-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="66744-107">Une partie de cette architecture est une base de données volumineuse de classes WMI utilisée pour effectuer des tâches de gestion à distance sur des objets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="66744-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="66744-108">Les fournisseurs WMI jouent le rôle d’intermédiaires entre WMI et un ou plusieurs objets gérés.</span><span class="sxs-lookup"><span data-stu-id="66744-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="66744-109">Lorsque WMI reçoit une demande d’une application de gestion pour les données qui ne sont pas disponibles dans le référentiel CIM ou pour les notifications d’événements que WMI ne prend pas en charge, il transfère la demande à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66744-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="66744-110">Les fournisseurs renvoient les données et les notifications d’événements pour les objets gérés qui sont spécifiques à leur domaine particulier.</span><span class="sxs-lookup"><span data-stu-id="66744-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="66744-111">Un fournisseur étend le schéma WMI des classes pour permettre à WMI de fonctionner avec de nouveaux types d’objets.</span><span class="sxs-lookup"><span data-stu-id="66744-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="66744-112">Le fournisseur WMI DNS définit des classes pour l’interrogation et la configuration d’un serveur DNS, ainsi que des zones DNS et des enregistrements DNS associés.</span><span class="sxs-lookup"><span data-stu-id="66744-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="66744-113">Le fournisseur WMI DNS expose un certain nombre d’objets DNS aux clients, y compris le serveur DNS, le domaine DNS et les objets de ressource DNS.</span><span class="sxs-lookup"><span data-stu-id="66744-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="66744-114">Grâce à ces objets, les clients sont en mesure d’effectuer des activités de gestion DNS.</span><span class="sxs-lookup"><span data-stu-id="66744-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="66744-115">À l’aide du fournisseur WMI DNS, vous pouvez créer vos propres outils pour effectuer la plupart des tâches d’administration de serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="66744-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="66744-116">Par exemple, vous pouvez créer, supprimer et afficher des zones et des enregistrements. réinitialiser les propriétés de serveur et de zone ; et effectuent des opérations d’administration de routine, telles que la mise à jour de la zone, le rechargement de la zone, l’actualisation de la zone, l’écriture de la zone dans un fichier ou un Active Directory, l’interruption et la reprise de la zone, l’effacement du cache, l’arrêt et le démarrage du service DNS, ainsi que l’affichage des statistiques.</span><span class="sxs-lookup"><span data-stu-id="66744-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="66744-117">Le fournisseur WMI DNS possède un ensemble de comportements uniques introuvables dans d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="66744-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="66744-118">Pour plus d’informations sur les classes, consultez la [Référence du fournisseur WMI DNS](dns-wmi-provider-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="66744-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 





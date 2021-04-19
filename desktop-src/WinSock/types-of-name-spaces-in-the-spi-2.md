---
description: Les trois types d’espaces de noms dans le SPI de Windows Sockets (Winsock) incluent des espaces de noms dynamiques, statiques et persistants.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Types d’espaces de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521098"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="b2f94-103">Types d’espaces de noms dans le SPI</span><span class="sxs-lookup"><span data-stu-id="b2f94-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="b2f94-104">Il existe trois types d’espaces de noms différents dans lesquels un service peut être inscrit :</span><span class="sxs-lookup"><span data-stu-id="b2f94-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="b2f94-105">Dynamique</span><span class="sxs-lookup"><span data-stu-id="b2f94-105">Dynamic</span></span>
-   <span data-ttu-id="b2f94-106">statique</span><span class="sxs-lookup"><span data-stu-id="b2f94-106">Static</span></span>
-   <span data-ttu-id="b2f94-107">Persistante</span><span class="sxs-lookup"><span data-stu-id="b2f94-107">Persistent</span></span>

<span data-ttu-id="b2f94-108">Les espaces de noms dynamiques permettent aux services de s’inscrire avec l’espace de noms à la volée, et pour que les clients découvrent les services disponibles au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b2f94-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="b2f94-109">Les espaces de noms dynamiques s’appuient souvent sur des diffusions pour indiquer la disponibilité continue d’un service réseau.</span><span class="sxs-lookup"><span data-stu-id="b2f94-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="b2f94-110">Les exemples d’espaces de noms dynamiques incluent l’espace de noms SAP utilisé dans un environnement NetWare et l’espace de noms NBP utilisé par AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="b2f94-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="b2f94-111">Les espaces de noms statiques requièrent que tous les services soient inscrits à l’avance, c’est-à-dire lorsque l’espace de noms est créé.</span><span class="sxs-lookup"><span data-stu-id="b2f94-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="b2f94-112">Le DNS est un exemple d’espace de noms statique.</span><span class="sxs-lookup"><span data-stu-id="b2f94-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="b2f94-113">Bien qu’il existe un moyen de résoudre les noms par programmation, il n’existe pas de méthode d’enregistrement des noms par programmation.</span><span class="sxs-lookup"><span data-stu-id="b2f94-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="b2f94-114">Les espaces de noms persistants permettent aux services de s’inscrire à l’espace de noms à la volée.</span><span class="sxs-lookup"><span data-stu-id="b2f94-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="b2f94-115">Contrairement aux espaces de noms dynamiques, toutefois, les espaces de noms persistants conservent les informations d’inscription dans un stockage non volatile où il reste jusqu’à ce que le service demande sa suppression.</span><span class="sxs-lookup"><span data-stu-id="b2f94-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="b2f94-116">Les espaces de noms persistants sont typified par des services d’annuaire tels que X. 500 et NDS (NetWare Directory Service).</span><span class="sxs-lookup"><span data-stu-id="b2f94-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="b2f94-117">Ces environnements permettent l’ajout, la suppression et la modification des propriétés du service.</span><span class="sxs-lookup"><span data-stu-id="b2f94-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="b2f94-118">En outre, l’objet de service représentant le service dans le service d’annuaire peut avoir plusieurs attributs associés au service.</span><span class="sxs-lookup"><span data-stu-id="b2f94-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="b2f94-119">L’attribut le plus important pour les applications clientes est les informations d’adressage du service.</span><span class="sxs-lookup"><span data-stu-id="b2f94-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 




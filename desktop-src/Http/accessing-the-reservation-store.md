---
title: Accès au magasin de réservations
description: L’API du serveur HTTP conserve la liste de réservation d’espace de noms pour tous les utilisateurs sur l’ordinateur.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Accès au magasin de réservations HTTP
- Magasin de réservation HTTP, accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379954"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="3f86e-105">Accès au magasin de réservations</span><span class="sxs-lookup"><span data-stu-id="3f86e-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="3f86e-106">L’API du serveur HTTP conserve la liste de réservation d’espace de noms pour tous les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3f86e-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="3f86e-107">Une entrée de réservation se compose d’un [URLPrefix](urlprefix-strings.md) et d’une liste de contrôle d’accès correspondante.</span><span class="sxs-lookup"><span data-stu-id="3f86e-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="3f86e-108">Chaque UrlPrefix dans le magasin a une liste de contrôle d’accès qui répertorie tous les utilisateurs qui sont autorisés à s’inscrire pour recevoir des demandes pour l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="3f86e-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="3f86e-109">Les utilisateurs disposant de privilèges de délégation peuvent déléguer des sous-arborescences de l’espace de noms dont ils sont propriétaires à d’autres utilisateurs ou supprimer des réservations existantes à l’aide des API de configuration.</span><span class="sxs-lookup"><span data-stu-id="3f86e-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="3f86e-110">Pour ajouter une réservation au magasin de réservation persistante, l’application appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre ID de configuration défini sur la valeur **HttpServiceConfigUrlAclInfo** .</span><span class="sxs-lookup"><span data-stu-id="3f86e-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="3f86e-111">L’API du serveur HTTP vérifie la propriété de l’espace de noms et l’ID de l’utilisateur avant d’ajouter une réservation au magasin.</span><span class="sxs-lookup"><span data-stu-id="3f86e-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="3f86e-112">L’API du serveur HTTP fournit également des fonctions pour interroger et supprimer les configurations de service pour les espaces de noms d’URL.</span><span class="sxs-lookup"><span data-stu-id="3f86e-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="3f86e-113">La fonction [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) appelée avec le paramètre ID de configuration défini sur les requêtes de valeur **HttpServiceConfigUrlAclInfo** et la fonction [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) supprime sur le magasin d’espaces de noms d’URL.</span><span class="sxs-lookup"><span data-stu-id="3f86e-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 





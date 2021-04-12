---
title: La base de données du service de noms RPC
description: Un service de noms est un service qui mappe des noms à des objets, et qui gère généralement les paires (nom, objet) d’une base de données.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Appel de procédure distante RPC, description, base de données de service de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462298"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="4decd-104">La base de données du service de noms RPC</span><span class="sxs-lookup"><span data-stu-id="4decd-104">The RPC Name Service Database</span></span>

<span data-ttu-id="4decd-105">Un service de noms est un service qui mappe des noms à des objets, et qui gère généralement les paires (nom, objet) d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="4decd-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="4decd-106">En règle générale, le nom est un nom logique facile à mémoriser et à utiliser par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4decd-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="4decd-107">Par exemple, un service de noms permet à un utilisateur d’utiliser le nom logique « laserprinter ».</span><span class="sxs-lookup"><span data-stu-id="4decd-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="4decd-108">Le service de noms mappe ce nom au nom spécifique au réseau utilisé par le serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4decd-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="4decd-109">Pour utiliser une explication simplifiée, le service de noms RPC mappe un nom à un handle de liaison et gère les mappages (nom, handle de liaison) dans la base de données du service de noms RPC.</span><span class="sxs-lookup"><span data-stu-id="4decd-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="4decd-110">Le service de noms RPC permet aux applications clientes d’utiliser un nom logique plutôt qu’une séquence de protocole et une adresse réseau spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4decd-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="4decd-111">L’utilisation du nom logique permet aux administrateurs réseau d’installer et de configurer plus facilement votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="4decd-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="4decd-112">Une entrée de base de données du service de noms RPC a l’un des attributs suivants : **serveur**, **groupe** ou **Profil**.</span><span class="sxs-lookup"><span data-stu-id="4decd-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="4decd-113">Dans l’implémentation Microsoft, les entrées ne peuvent avoir qu’un seul attribut, de sorte que ces entrées sont également appelées des entrées de serveur, des entrées de groupe et des entrées de profil.</span><span class="sxs-lookup"><span data-stu-id="4decd-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="4decd-114">L’entrée de serveur se compose d’UUID d’interface, d’UUID d’objets (nécessaires lorsque le serveur implémente des points d’entrée multiples), d’une adresse réseau, d’une séquence de protocole et de toutes les informations de point de terminaison associées à des points de terminaison connus.</span><span class="sxs-lookup"><span data-stu-id="4decd-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="4decd-115">Lorsqu’un point de terminaison dynamique est utilisé, les informations de point de terminaison sont conservées dans la base de données de mappage des points de terminaison et non dans la base de données du service de noms, et le point de terminaison est résolu comme tout autre point de terminaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="4decd-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="4decd-116">Les entrées de serveur sont gérées par des fonctions qui commencent par le préfixe « RpcNsBinding ».</span><span class="sxs-lookup"><span data-stu-id="4decd-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="4decd-117">L’entrée de groupe peut contenir des entrées de serveur ou d’autres entrées de groupe.</span><span class="sxs-lookup"><span data-stu-id="4decd-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="4decd-118">Les entrées de groupe sont gérées par des fonctions qui commencent par le préfixe « RpcNsGroup ».</span><span class="sxs-lookup"><span data-stu-id="4decd-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="4decd-119">L’entrée de profil peut contenir des entrées de profil, de groupe ou de serveur.</span><span class="sxs-lookup"><span data-stu-id="4decd-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="4decd-120">Les entrées de profil sont gérées par les fonctions qui commencent par le préfixe « RpcNsProfile ».</span><span class="sxs-lookup"><span data-stu-id="4decd-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="4decd-121">Cette section présente une vue d’ensemble de la base de données de service de noms dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4decd-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="4decd-122">Instructions pour les applications de service de noms</span><span class="sxs-lookup"><span data-stu-id="4decd-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="4decd-123">Vue d’ensemble de l’entrée Service Name</span><span class="sxs-lookup"><span data-stu-id="4decd-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="4decd-124">Critères pour les entrées de service de nom</span><span class="sxs-lookup"><span data-stu-id="4decd-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="4decd-125">Nettoyage de l’entrée du service de noms</span><span class="sxs-lookup"><span data-stu-id="4decd-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="4decd-126">Ce qui se passe lors d’une requête</span><span class="sxs-lookup"><span data-stu-id="4decd-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="4decd-127">Utilisation de Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="4decd-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="4decd-128">Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)</span><span class="sxs-lookup"><span data-stu-id="4decd-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="4decd-129">Syntaxe de nom</span><span class="sxs-lookup"><span data-stu-id="4decd-129">Name Syntax</span></span>](name-syntax.md)

 

 





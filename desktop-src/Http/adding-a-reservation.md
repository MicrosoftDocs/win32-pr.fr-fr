---
title: Ajout d’une réservation
description: La base de données de routage contient la liste des réservations.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104508190"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="0a39e-103">Ajout d’une réservation</span><span class="sxs-lookup"><span data-stu-id="0a39e-103">Adding a Reservation</span></span>

<span data-ttu-id="0a39e-104">La base de données de routage contient la liste des réservations.</span><span class="sxs-lookup"><span data-stu-id="0a39e-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="0a39e-105">La liste de réservation se compose des utilisateurs qui sont autorisés à accéder à l’espace de noms, ainsi que du niveau d’accès pour chaque utilisateur répertorié sous la réservation.</span><span class="sxs-lookup"><span data-stu-id="0a39e-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="0a39e-106">Lorsque des réservations sont ajoutées ou supprimées, la base de données de routage est recherchée pour déterminer les privilèges d’accès.</span><span class="sxs-lookup"><span data-stu-id="0a39e-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="0a39e-107">En plus de vérifier l’ID des utilisateurs, l’API du serveur HTTP vérifie également la présence de conflits dans les réservations existantes avant d’installer une nouvelle réservation.</span><span class="sxs-lookup"><span data-stu-id="0a39e-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="0a39e-108">**Pour ajouter une nouvelle réservation**</span><span class="sxs-lookup"><span data-stu-id="0a39e-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="0a39e-109">Si le numéro de port dans le UrlPrefix a des réservations ou des inscriptions pour un schéma différent du schéma dans le UrlPrefix, l’inscription échoue.</span><span class="sxs-lookup"><span data-stu-id="0a39e-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="0a39e-110">Les protocoles HTTP et HTTPs ne peuvent pas être pris en charge sur le même port.</span><span class="sxs-lookup"><span data-stu-id="0a39e-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="0a39e-111">Recherchez le compartiment approprié pour l’inscription (voir la section [routage des demandes entrantes](routing-incoming-requests.md) ), en fonction du type d’hôte.</span><span class="sxs-lookup"><span data-stu-id="0a39e-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="0a39e-112">Les étapes restantes sont relatives à ce compartiment.</span><span class="sxs-lookup"><span data-stu-id="0a39e-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="0a39e-113">Sélectionnez entrées de réservation avec les composants de schéma, d’hôte et de port qui correspondent au UrlPrefix réservé.</span><span class="sxs-lookup"><span data-stu-id="0a39e-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="0a39e-114">À partir de celles-ci, localisez l’entrée ayant le *relativeUri* correspondant le plus long, qui n’est pas égal au relativeUri dans la réservation (autrement dit, le *nœud parent*).</span><span class="sxs-lookup"><span data-stu-id="0a39e-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="0a39e-115">Si l’entrée existe, évaluez les droits d’accès en fonction de la liste de contrôle d’accès assignée à cette entrée.</span><span class="sxs-lookup"><span data-stu-id="0a39e-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="0a39e-116">Si un nœud parent est introuvable, il s’agit d’une réservation avec un relativeUri vide ou une *réservation racine*.</span><span class="sxs-lookup"><span data-stu-id="0a39e-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="0a39e-117">Accordez des droits d’accès uniquement si l’appelant est inscrit sous les comptes LocalSystem ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="0a39e-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="0a39e-118">Si des droits d’accès sont accordés, vérifiez les réservations en double.</span><span class="sxs-lookup"><span data-stu-id="0a39e-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="0a39e-119">Si une entrée de réservation existe avec les mêmes schéma, port, hôte et relativeUri, le code d’une erreur \_ \_ existe déjà est retourné.</span><span class="sxs-lookup"><span data-stu-id="0a39e-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="0a39e-120">La mise à jour d’une entrée existante doit être effectuée en deux étapes : supprimer l’entrée et en ajouter une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="0a39e-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="0a39e-121">Si les étapes ci-dessus ont réussie, une nouvelle entrée de réservation est entrée dans la base de données de réservation.</span><span class="sxs-lookup"><span data-stu-id="0a39e-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="0a39e-122">La nouvelle entrée est créée avec la liste de contrôle d’accès spécifiée et n’hérite pas des ACL de l’entrée *parente* .</span><span class="sxs-lookup"><span data-stu-id="0a39e-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="0a39e-123">Les exemples suivants illustrent le processus de réservation.</span><span class="sxs-lookup"><span data-stu-id="0a39e-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="0a39e-124">Réservation 1 : `https://+:80/vroot/subdir/` par l’administrateur de l’utilisateur A et l’utilisateur C parvient à entrer dans le compartiment « + ».</span><span class="sxs-lookup"><span data-stu-id="0a39e-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="0a39e-125">Réservation 2 : `https://adatum.com:80/vroot/` par l’administrateur pour l’utilisateur B et est entré dans le compartiment « hôte explicite ».</span><span class="sxs-lookup"><span data-stu-id="0a39e-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="0a39e-126">Réservation 3 : `https://adatum.com:80/vroot/subdir/otherdir/` par l’utilisateur B pour l’utilisateur C s’est correctement déroulée en raison de la réservation 2.</span><span class="sxs-lookup"><span data-stu-id="0a39e-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="0a39e-127">Réservation 4 : `https://+:80/vroot/subdir/otherdir/` par l’utilisateur A pour l’utilisateur E s’est correctement déroulée en raison de la réservation 1.</span><span class="sxs-lookup"><span data-stu-id="0a39e-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="0a39e-128">Réservation 5 : `https://adatum.com:80/vroot/subdir/otherdir/` par l’utilisateur A pour l’utilisateur E échoue.</span><span class="sxs-lookup"><span data-stu-id="0a39e-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="0a39e-129">Accès refusé en raison de la réservation 2.</span><span class="sxs-lookup"><span data-stu-id="0a39e-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="0a39e-130">Réservation 6 : `https://+:80/vroot/subdir/` par l’administrateur de l’utilisateur A échoue.</span><span class="sxs-lookup"><span data-stu-id="0a39e-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="0a39e-131">La réservation est en conflit avec la réservation 1.</span><span class="sxs-lookup"><span data-stu-id="0a39e-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="0a39e-132">Réservation 7 : `https://adatum.com:80/newroot/` par l’utilisateur a pour l’utilisateur a échoue.</span><span class="sxs-lookup"><span data-stu-id="0a39e-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="0a39e-133">Accès refusé en raison d’une réservation racine implicite de `https://adatum.com:80/` pour LocalSystem ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="0a39e-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="0a39e-134">Les réservations peuvent affecter le jeu d’URL dans les demandes remises à un processus qui a précédemment inscrit un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="0a39e-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="0a39e-135">Par exemple, considérez le scénario suivant.</span><span class="sxs-lookup"><span data-stu-id="0a39e-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="0a39e-136">Inscription : `https://adatum.com:80/vroot/` par application 1 pour l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="0a39e-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="0a39e-137">Une demande pour `https://adatum.com:80/vroot/subdir/file.htm` est remise à l’application 1.</span><span class="sxs-lookup"><span data-stu-id="0a39e-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="0a39e-138">Réservation : `https://+:80/vroot/subdir/` pour l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="0a39e-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="0a39e-139">Une requête pour `https://adatum.com:80/vroot/subdir/file.htm` est maintenant rejetée.</span><span class="sxs-lookup"><span data-stu-id="0a39e-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="0a39e-140">Inscription : `https://adatum.com:80/vroot/subdir/` par application 2 pour l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="0a39e-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="0a39e-141">Une demande pour `https://adatum.com:80/vroot/subdir/file.htm` est remise à l’application 2.</span><span class="sxs-lookup"><span data-stu-id="0a39e-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 





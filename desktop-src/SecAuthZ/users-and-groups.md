---
description: Explique la définition des utilisateurs et des groupes dans l’API du gestionnaire d’autorisations.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Utilisateurs et groupes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529478"
---
# <a name="users-and-groups"></a><span data-ttu-id="04bf0-103">Utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="04bf0-103">Users and Groups</span></span>

<span data-ttu-id="04bf0-104">Dans le gestionnaire d’autorisations, les destinataires de la stratégie d’autorisation sont représentés par les groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="04bf0-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="04bf0-105">Utilisateurs et groupes Windows</span><span class="sxs-lookup"><span data-stu-id="04bf0-105">Windows Users and Groups</span></span>

    <span data-ttu-id="04bf0-106">Ces groupes incluent les utilisateurs, les ordinateurs et les groupes intégrés pour les principaux de sécurité.</span><span class="sxs-lookup"><span data-stu-id="04bf0-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="04bf0-107">Groupes de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="04bf0-107">LDAP Query Groups</span></span>

    <span data-ttu-id="04bf0-108">L’appartenance à ces groupes est calculée dynamiquement en fonction des besoins à partir des requêtes LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="04bf0-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="04bf0-109">Un groupe de requêtes LDAP est un type de groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="04bf0-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="04bf0-110">Groupes d’applications de base</span><span class="sxs-lookup"><span data-stu-id="04bf0-110">Basic Application Groups</span></span>

    <span data-ttu-id="04bf0-111">Ces groupes sont constitués de groupes de requêtes LDAP, d’utilisateurs et de groupes Windows et d’autres groupes d’applications de base.</span><span class="sxs-lookup"><span data-stu-id="04bf0-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="04bf0-112">Utilisateurs et groupes Windows</span><span class="sxs-lookup"><span data-stu-id="04bf0-112">Windows Users and Groups</span></span>

<span data-ttu-id="04bf0-113">Ils sont les mêmes que les utilisateurs et les groupes utilisés dans le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="04bf0-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="04bf0-114">Groupes de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="04bf0-114">LDAP Query Groups</span></span>

<span data-ttu-id="04bf0-115">Dans le gestionnaire d’autorisations, vous pouvez utiliser des requêtes LDAP pour faire correspondre les attributs de l’utilisateur avec ceux de l’objet de l’utilisateur dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="04bf0-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="04bf0-116">Par exemple, la requête suivante recherche tout le monde sauf Andy.</span><span class="sxs-lookup"><span data-stu-id="04bf0-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="04bf0-117">La requête suivante recherche tous les membres de l’alias de l’utilisateur sur www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="04bf0-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="04bf0-118">Groupes d’applications de base</span><span class="sxs-lookup"><span data-stu-id="04bf0-118">Basic Application Groups</span></span>

<span data-ttu-id="04bf0-119">Dans l’API du gestionnaire d’autorisations, un groupe d’applications est représenté par un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="04bf0-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="04bf0-120">Un groupe d’applications de base est un type de groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="04bf0-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="04bf0-121">Pour définir l’appartenance à un groupe d’applications de base, définissez qui est membre et définissez qui n’est pas membre.</span><span class="sxs-lookup"><span data-stu-id="04bf0-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="04bf0-122">Ces deux étapes sont effectuées de la même façon.</span><span class="sxs-lookup"><span data-stu-id="04bf0-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="04bf0-123">Spécifiez zéro, un ou plusieurs utilisateurs et groupes Windows, des groupes d’applications de base ou des groupes de requêtes LDAP définis précédemment.</span><span class="sxs-lookup"><span data-stu-id="04bf0-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="04bf0-124">L’appartenance du groupe d’applications de base est calculée en supprimant tous les non-membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="04bf0-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="04bf0-125">Le gestionnaire d’autorisations le fait automatiquement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="04bf0-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="04bf0-126">La non-appartenance à un groupe d’applications de base est prioritaire sur l’appartenance.</span><span class="sxs-lookup"><span data-stu-id="04bf0-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="04bf0-127">Les définitions d’appartenance circulaire ne sont pas autorisées ; ils génèrent le message d’erreur suivant : «impossible d’ajouter GroupName.</span><span class="sxs-lookup"><span data-stu-id="04bf0-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="04bf0-128">Le problème suivant s’est produit : une boucle a été détectée.»</span><span class="sxs-lookup"><span data-stu-id="04bf0-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="04bf0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04bf0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04bf0-130">Définition de groupes d’utilisateurs en C++</span><span class="sxs-lookup"><span data-stu-id="04bf0-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 




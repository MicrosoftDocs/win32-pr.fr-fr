---
title: Gestion des utilisateurs
description: Les comptes d’utilisateur sont créés et stockés en tant qu’objets dans Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, gestion des utilisateurs
- utilisateurs AD
- utilisateurs Active Directory, gestion des utilisateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1105132c6836e108a416331b2f4a6ad666c03d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839297"
---
# <a name="managing-users"></a><span data-ttu-id="7357d-106">Gestion des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7357d-106">Managing Users</span></span>

<span data-ttu-id="7357d-107">Les comptes d’utilisateur sont créés et stockés en tant qu’objets dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7357d-107">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="7357d-108">Ces objets utilisateur représentent les utilisateurs et les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7357d-108">These user objects represent users and computers.</span></span> <span data-ttu-id="7357d-109">Cette section définit ce que sont les utilisateurs et comment ils sont utilisés, et explique comment gérer par programmation les utilisateurs dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7357d-109">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="7357d-110">Cette section aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="7357d-110">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="7357d-111">Utilisateurs dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7357d-111">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="7357d-112">Principaux de sécurité</span><span class="sxs-lookup"><span data-stu-id="7357d-112">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="7357d-113">Qu’est-ce qu’un utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="7357d-113">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="7357d-114">Exemple de code pour la liaison au conteneur Users</span><span class="sxs-lookup"><span data-stu-id="7357d-114">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="7357d-115">Attributs d’objet utilisateur</span><span class="sxs-lookup"><span data-stu-id="7357d-115">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="7357d-116">Création d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="7357d-116">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="7357d-117">Suppression d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7357d-117">Deleting a user.</span></span> <span data-ttu-id="7357d-118">Un utilisateur est supprimé de la même façon que tout autre objet dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7357d-118">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="7357d-119">Pour plus d’informations sur la suppression d’objets, consultez [création et suppression d’objets dans Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="7357d-119">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="7357d-120">Énumération des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7357d-120">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="7357d-121">Interrogation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7357d-121">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="7357d-122">Déplacement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7357d-122">Moving users.</span></span> <span data-ttu-id="7357d-123">Un utilisateur est déplacé de la même façon que tout autre objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7357d-123">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="7357d-124">Pour plus d’informations sur le déplacement d’objets Active Directory, consultez [déplacement d’objets](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7357d-124">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="7357d-125">Gestion des utilisateurs sur les serveurs membres et Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="7357d-125">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 





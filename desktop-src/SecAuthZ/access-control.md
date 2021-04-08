---
description: Le contrôle d’accès fait référence à des fonctionnalités de sécurité qui contrôlent qui peut accéder aux ressources dans le système d’exploitation. Les applications appellent des fonctions de contrôle d’accès pour définir qui peut accéder à des ressources spécifiques ou contrôler l’accès aux ressources fournies par l’application.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034390"
---
# <a name="access-control-authorization"></a><span data-ttu-id="fd7ac-104">Access Control (autorisation)</span><span class="sxs-lookup"><span data-stu-id="fd7ac-104">Access Control (Authorization)</span></span>

<span data-ttu-id="fd7ac-105">Le contrôle d’accès fait référence à des fonctionnalités de sécurité qui contrôlent qui peut accéder aux ressources dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fd7ac-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="fd7ac-106">Les applications appellent des fonctions de contrôle d’accès pour définir qui peut accéder à des ressources spécifiques ou contrôler l’accès aux ressources fournies par l’application.</span><span class="sxs-lookup"><span data-stu-id="fd7ac-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="fd7ac-107">Cette vue d’ensemble décrit le modèle de sécurité pour le contrôle de l’accès aux objets Windows, tels que les fichiers, et pour le contrôle de l’accès aux fonctions d’administration, telles que la définition de l’heure système ou de l’audit des actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd7ac-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="fd7ac-108">La rubrique [Access Control Model](access-control-model.md) fournit une description détaillée des parties du contrôle d’accès et de la façon dont elles interagissent les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="fd7ac-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="fd7ac-109">Les rubriques suivantes décrivent le contrôle d’accès :</span><span class="sxs-lookup"><span data-stu-id="fd7ac-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="fd7ac-110">Sécurité de niveau C2</span><span class="sxs-lookup"><span data-stu-id="fd7ac-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="fd7ac-111">Modèle de Access Control</span><span class="sxs-lookup"><span data-stu-id="fd7ac-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="fd7ac-112">Langage de définition du descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd7ac-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="fd7ac-113">Privilèges</span><span class="sxs-lookup"><span data-stu-id="fd7ac-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="fd7ac-114">Génération de l’audit</span><span class="sxs-lookup"><span data-stu-id="fd7ac-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="fd7ac-115">Objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="fd7ac-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="fd7ac-116">Access Control de bas niveau</span><span class="sxs-lookup"><span data-stu-id="fd7ac-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="fd7ac-117">Les tâches de contrôle d’accès courantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd7ac-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="fd7ac-118">Comment les DACL contrôlent l’accès à un objet</span><span class="sxs-lookup"><span data-stu-id="fd7ac-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="fd7ac-119">Contrôle de la création d’objets enfants en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="fd7ac-120">Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’un objet</span><span class="sxs-lookup"><span data-stu-id="fd7ac-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="fd7ac-121">Demande de droits d’accès à un objet</span><span class="sxs-lookup"><span data-stu-id="fd7ac-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="fd7ac-122">Les rubriques suivantes fournissent un exemple de code pour les tâches de contrôle d’accès :</span><span class="sxs-lookup"><span data-stu-id="fd7ac-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="fd7ac-123">Modification des listes de contrôle d’accès d’un objet en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="fd7ac-124">Création d’un descripteur de sécurité pour un nouvel objet en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="fd7ac-125">Contrôle de la création d’objets enfants en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="fd7ac-126">Activation et désactivation des privilèges en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="fd7ac-127">Recherche d’un SID dans un jeton d’accès en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="fd7ac-128">Recherche du propriétaire d’un objet de fichier en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="fd7ac-129">Appropriation d’objets en C++</span><span class="sxs-lookup"><span data-stu-id="fd7ac-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="fd7ac-130">Création d’une liste DACL</span><span class="sxs-lookup"><span data-stu-id="fd7ac-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 

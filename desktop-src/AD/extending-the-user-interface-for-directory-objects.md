---
title: Extension de l’interface utilisateur pour les objets d’annuaire
description: Avec Microsoft Windows 2000 et versions ultérieures, les composants logiciels enfichables de la console MMC (Microsoft Management Console), tels que le composant logiciel enfichable utilisateurs et ordinateurs Active Directory, pour l’administration de Active Directory Domain Services, sont disponibles.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, extension de l’interface utilisateur
- objets AD, extension de l’interface utilisateur pour les objets d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671281"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="90c8c-105">Extension de l’interface utilisateur pour les objets d’annuaire</span><span class="sxs-lookup"><span data-stu-id="90c8c-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="90c8c-106">Avec Microsoft Windows 2000 et versions ultérieures, les composants logiciels enfichables de la console MMC (Microsoft Management Console), tels que le composant logiciel enfichable utilisateurs et ordinateurs Active Directory, pour l’administration de Active Directory Domain Services, sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="90c8c-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="90c8c-107">En outre, l’interpréteur de commandes Windows 2000 comprend des interfaces utilisateur permettant de rechercher des objets qui résident dans le répertoire et de lire et d’écrire des propriétés.</span><span class="sxs-lookup"><span data-stu-id="90c8c-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="90c8c-108">Cette section explique comment étendre l’interface utilisateur pour afficher et gérer des objets Active Directory Domain Services dans le shell Windows et Active Directory des composants logiciels enfichables d’administration. Cette section décrit également ce qui est nécessaire pour déployer les extensions d’interface utilisateur sur les ordinateurs de bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="90c8c-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="90c8c-109">Plus précisément, cette section aborde les points suivants :</span><span class="sxs-lookup"><span data-stu-id="90c8c-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="90c8c-110">À propos des interfaces utilisateur Active Directory</span><span class="sxs-lookup"><span data-stu-id="90c8c-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="90c8c-111">Spécificateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="90c8c-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="90c8c-112">Noms complets des classes et des attributs</span><span class="sxs-lookup"><span data-stu-id="90c8c-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="90c8c-113">Icônes de classe</span><span class="sxs-lookup"><span data-stu-id="90c8c-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="90c8c-114">Affichage des conteneurs en tant que nœuds terminaux</span><span class="sxs-lookup"><span data-stu-id="90c8c-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="90c8c-115">Modification des interfaces utilisateur existantes</span><span class="sxs-lookup"><span data-stu-id="90c8c-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="90c8c-116">Extension de l’interface utilisateur pour les nouvelles classes d’objets</span><span class="sxs-lookup"><span data-stu-id="90c8c-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="90c8c-117">Pages de propriétés à utiliser avec les spécificateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="90c8c-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="90c8c-118">Menus contextuels à utiliser avec les spécificateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="90c8c-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="90c8c-119">Assistants de création d’objets</span><span class="sxs-lookup"><span data-stu-id="90c8c-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="90c8c-120">Utilisation de boîtes de dialogue standard pour la gestion des objets dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="90c8c-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="90c8c-121">Gestionnaires de notifications d’administration</span><span class="sxs-lookup"><span data-stu-id="90c8c-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="90c8c-122">Distribution des composants de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="90c8c-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="90c8c-123">Comment les applications doivent utiliser des spécificateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="90c8c-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="90c8c-124">Débogage d’une extension de Active Directory</span><span class="sxs-lookup"><span data-stu-id="90c8c-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 





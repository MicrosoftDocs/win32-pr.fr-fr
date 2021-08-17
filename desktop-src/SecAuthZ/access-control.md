---
description: Le contrôle d’accès fait référence à des fonctionnalités de sécurité qui contrôlent qui peut accéder aux ressources dans le système d’exploitation. Les applications appellent des fonctions de contrôle d’accès pour définir qui peut accéder à des ressources spécifiques ou contrôler l’accès aux ressources fournies par l’application.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34be93577446066fcaf7e01e634c60632c68c430198a375eadc2efbcec3e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785639"
---
# <a name="access-control-authorization"></a>Access Control (autorisation)

Le contrôle d’accès fait référence à des fonctionnalités de sécurité qui contrôlent qui peut accéder aux ressources dans le système d’exploitation. Les applications appellent des fonctions de contrôle d’accès pour définir qui peut accéder à des ressources spécifiques ou contrôler l’accès aux ressources fournies par l’application.

cette vue d’ensemble décrit le modèle de sécurité pour le contrôle de l’accès aux objets Windows, tels que les fichiers, et pour le contrôle de l’accès aux fonctions d’administration, telles que la définition de l’heure système ou de l’audit des actions de l’utilisateur. La rubrique [Access Control Model](access-control-model.md) fournit une description détaillée des parties du contrôle d’accès et de la façon dont elles interagissent les unes avec les autres.

Les rubriques suivantes décrivent le contrôle d’accès :

-   [Sécurité de niveau C2](c2-level-security.md)
-   [Modèle de Access Control](access-control-model.md)
-   [Langage de définition du descripteur de sécurité](security-descriptor-definition-language.md)
-   [Privilèges](privileges.md)
-   [Génération de l’audit](audit-generation.md)
-   [Objets sécurisables](securable-objects.md)
-   [Access Control de bas niveau](low-level-access-control.md)

Les tâches de contrôle d’accès courantes sont les suivantes :

-   [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md)
-   [Contrôle de la création d’objets enfants en C++](controlling-child-object-creation-in-c--.md)
-   [Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’un objet](aces-to-control-access-to-an-object-s-properties.md)
-   [Demande de droits d’accès à un objet](requesting-access-rights-to-an-object.md)

Les rubriques suivantes fournissent un exemple de code pour les tâches de contrôle d’accès :

-   [Modification des listes de contrôle d’accès d’un objet en C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Contrôle de la création d’objets enfants en C++](controlling-child-object-creation-in-c--.md)
-   [Activation et désactivation des privilèges en C++](enabling-and-disabling-privileges-in-c--.md)
-   [Recherche d’un SID dans un jeton d’accès en C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Recherche du propriétaire d’un objet de fichier en C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Appropriation d’objets en C++](taking-object-ownership-in-c--.md)
-   [Création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 

---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour définir des autorisations en C++ en créant un magasin de stratégies d’autorisation.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Définition des autorisations en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013699"
---
# <a name="defining-permissions-in-c"></a>Définition des autorisations en C++

Dans le gestionnaire d’autorisations, vous définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation.

Pour plus d’informations sur la définition d’autorisations avec des listes de contrôle d’accès, consultez [définition d’autorisations avec des ACL en C++](defining-permissions-with-acls-in-c--.md).

**Pour définir des autorisations d’accès**

1.  Créez le magasin dans lequel la stratégie d’autorisation est définie :<dl>

[Création d’un objet du magasin de stratégies d’autorisation en C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Créer une section dans le magasin de stratégies d’autorisation pour une application spécifique :<dl>

[Création d’un objet d’application en C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Définissez les opérations que l’application implémente pour accéder aux ressources et les modifier :<dl>

[Définition d’opérations en C++](defining-operations-in-c--.md)  
    </dl>
4.  Regroupez les opérations en tâches de haut niveau que les utilisateurs souhaitent effectuer :<dl>

[Regroupement d’opérations en tâches en C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Définir des rôles composés de groupes de tâches :<dl>

[Regroupement de tâches en rôles en C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Un utilisateur affecté à un rôle a l’autorisation d’effectuer n’importe quelle tâche affectée à ce rôle.
6.  Créer des scripts pour qualifier l’accès aux tâches au moment de l’exécution :<dl>

[Accès éligible avec la logique métier en C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Cette étape est facultative.
7.  Définir des groupes d’utilisateurs :<dl>

[Définition de groupes d’utilisateurs en C++](defining-groups-of-users-in-c--.md)  
    </dl>Ces groupes peuvent ensuite être affectés à des rôles pour déterminer les tâches qu’ils peuvent effectuer.
8.  Ajouter des utilisateurs à des groupes d’utilisateurs :<dl>

[Ajout d’utilisateurs à un groupe d’applications en C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 




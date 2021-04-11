---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour définir des autorisations dans le script en créant un magasin de stratégies d’autorisation.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Définition des autorisations dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952576"
---
# <a name="defining-permissions-in-script"></a>Définition des autorisations dans le script

Dans le gestionnaire d’autorisations, vous définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation.

**Pour définir des autorisations d’accès**

1.  Créez le magasin dans lequel la stratégie d’autorisation est définie :<dl>

[Création d’un magasin de stratégies d’autorisation dans le script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Créer une section dans le magasin de stratégies d’autorisation pour une application spécifique :<dl>

[Création d’un objet d’application dans un script](creating-an-application-object-in-script.md)  
    </dl>
3.  Définissez les opérations que l’application implémente pour accéder aux ressources et les modifier :<dl>

[Définition des opérations dans le script](defining-operations-in-script.md)  
    </dl>
4.  Regroupez les opérations en tâches de haut niveau que les utilisateurs souhaitent effectuer :<dl>

[Regroupement d’opérations en tâches dans un script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Définir des rôles composés de groupes de tâches :<dl>

[Regroupement de tâches en rôles dans le script](grouping-tasks-into-roles-in-script.md)  
    </dl>Un utilisateur affecté à un rôle a l’autorisation d’effectuer n’importe quelle tâche affectée à ce rôle.
6.  Créer des scripts pour qualifier l’accès aux tâches au moment de l’exécution :<dl>

[Accès éligible avec la logique métier dans le script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Cette étape est facultative.
7.  Définir des groupes d’utilisateurs :<dl>

[Définition de groupes d’utilisateurs dans le script](defining-groups-of-users-in-script.md)  
    </dl>Ces groupes peuvent ensuite être affectés à des rôles pour déterminer les tâches qu’ils peuvent effectuer.
8.  Ajouter des utilisateurs à des groupes d’utilisateurs :<dl>

[Ajout d’utilisateurs à un groupe d’applications dans le script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 




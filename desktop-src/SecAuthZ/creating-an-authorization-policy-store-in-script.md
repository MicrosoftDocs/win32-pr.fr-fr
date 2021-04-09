---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour créer un magasin de stratégies d’autorisation dans le script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Création d’un magasin de stratégies d’autorisation dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114539"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Création d’un magasin de stratégies d’autorisation dans le script

Créer une stratégie d’autorisation avant ou pendant l’installation d’une application.

Lorsque vous utilisez l’API du gestionnaire d’autorisations pour créer une stratégie d’autorisation, suivez les instructions fournies dans les rubriques suivantes.



| Rubrique                                                                                                                  | Description                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Création d’un objet du magasin de stratégies d’autorisation dans le script](creating-an-authorization-policy-store-object-in-script.md) | Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications.                                                                                                                                       |
| [Création d’un objet d’application dans un script](creating-an-application-object-in-script.md)                               | Pour chaque application qui utilise un magasin de stratégies d’autorisation, vous devez créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) et l’enregistrer dans un magasin de stratégies.                                                                                                |
| [Définition des opérations dans le script](defining-operations-in-script.md)                                                     | Une opération est une fonction ou une méthode de bas niveau d’une application.                                                                                                                                                                                              |
| [Regroupement d’opérations en tâches dans un script](grouping-operations-into-tasks-in-script.md)                               | Une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer. Les tâches sont constituées d’opérations, qui sont des fonctions de bas niveau et des méthodes de l’application.                                                                                    |
| [Regroupement de tâches en rôles dans le script](grouping-tasks-into-roles-in-script.md)                                         | Un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer.                                                                                                                                                                     |
| [Définition de groupes d’utilisateurs dans le script](defining-groups-of-users-in-script.md)                                           | Un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective. Un objet **IAzApplicationGroup** peut également inclure d’autres objets **IAzApplicationGroup** en tant que membres. |
| [Ajout d’utilisateurs à un groupe d’applications dans le script](adding-users-to-an-application-group-in-script.md)                   | Un groupe d’applications est un groupe d’utilisateurs et de groupes d’utilisateurs. Comme un groupe d’applications peut contenir d’autres groupes d’applications, les groupes d’utilisateurs peuvent être imbriqués. Un groupe d’applications est représenté par un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .    |



 

 

 




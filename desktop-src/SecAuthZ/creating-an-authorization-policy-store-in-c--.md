---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour créer un magasin de stratégies d’autorisation en C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Création d’un magasin de stratégies d’autorisation en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114138"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Création d’un magasin de stratégies d’autorisation en C++

Créer une stratégie d’autorisation avant ou pendant l’installation d’une application.

Lorsque vous utilisez l’API du gestionnaire d’autorisations pour créer une stratégie d’autorisation, suivez les instructions fournies dans les rubriques suivantes.



| Rubrique                                                                                                            | Description                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Création d’un objet du magasin de stratégies d’autorisation en C++](creating-an-authorization-policy-store-object-in-c--.md) | Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications. Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin.              |
| [Création d’un objet d’application en C++](creating-an-application-object-in-c--.md)                               | Un magasin de stratégies d’autorisation contient des informations de stratégie d’autorisation pour une ou plusieurs applications. Pour chaque application qui utilise ce magasin de stratégies, vous devez créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) et l’enregistrer dans un magasin de stratégies. |
| [Définition d’opérations en C++](defining-operations-in-c--.md)                                                     | Dans le gestionnaire d’autorisations, une opération est une fonction ou une méthode de bas niveau d’une application.                                                                                                                                                               |
| [Regroupement d’opérations en tâches en C++](grouping-operations-into-tasks-in-c--.md)                               | Dans le gestionnaire d’autorisations, une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer. Les tâches sont constituées d’opérations, qui sont des fonctions de bas niveau et des méthodes de l’application.                                                     |
| [Regroupement de tâches en rôles en C++](grouping-tasks-into-roles-in-c--.md)                                         | Dans le gestionnaire d’autorisations, un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer.                                                                                                                                      |
| [Définition de groupes d’utilisateurs en C++](defining-groups-of-users-in-c--.md)                                           | Dans le gestionnaire d’autorisations, un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective.                                                                       |
| [Ajout d’utilisateurs à un groupe d’applications en C++](adding-users-to-an-application-group-in-c--.md)                   | Dans le gestionnaire d’autorisations, un groupe d’applications est un groupe d’utilisateurs et de groupes d’utilisateurs. Comme un groupe d’applications peut contenir d’autres groupes d’applications, les groupes d’utilisateurs peuvent être imbriqués.                                                                          |



 

 

 




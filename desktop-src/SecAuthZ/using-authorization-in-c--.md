---
description: Utilisez l’API du gestionnaire d’autorisations pour contrôler l’accès aux ressources de l’application.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Utilisation de l’autorisation en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523318"
---
# <a name="using-authorization-in-c"></a>Utilisation de l’autorisation en C++

Vous pouvez utiliser l’API du gestionnaire d’autorisations pour contrôler l’accès aux ressources de l’application.

Si vous disposez d’une solution de contrôle d’accès existante basée sur des [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) et que vous souhaitez éviter de convertir cette solution pour utiliser le gestionnaire d’autorisations, vous pouvez continuer à utiliser les listes de contrôle d’accès pour contrôler l’accès aux ressources. Pour plus d’informations sur le contrôle de l’accès aux ressources à l’aide de listes de contrôle d’accès, consultez [définition d’autorisations avec des ACL en c++](defining-permissions-with-acls-in-c--.md), [établissement d’un contexte client à partir d’un SID en c++](establishing-a-client-context-from-a-sid-in-c--.md)et [vérification de l’accès client avec des ACL en c++](verifying-client-access-with-acls-in-c--.md).

> [!Note]  
> Pour les grandes entreprises, il existe un compromis entre la surcharge administrative et les performances. À mesure que le nombre de ressources et d’utilisateurs sécurisés augmente, l’administration des ACL devient plus complexe. Les performances ne sont pas affectées, car toutes les informations requises sur les droits d’accès sont distribuées aux ressources sécurisées. Les performances du gestionnaire d’autorisations sont affectées par la mise à l’échelle.

 

Pour plus d’informations sur les autres tâches d’autorisation, consultez [prise en charge des tâches pour l’autorisation en C++](supporting-tasks-for-authorization-in-c--.md).



| Rubrique                                                                                                                | Description                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Définition des autorisations en C++](defining-permissions-in-c--.md)                                                       | Définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation. |
| [Vérification de l’accès client à une ressource demandée en C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Vérifiez si le client a accès à une ou plusieurs opérations.                                           |
| [Délégation de la définition des autorisations en C++](delegating-the-defining-of-permissions-in-c--.md)                   | Déléguez l’administration des magasins de stratégies d’autorisation stockés dans Active Directory.          |



 

 

 

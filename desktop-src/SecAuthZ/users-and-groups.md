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
# <a name="users-and-groups"></a>Utilisateurs et groupes

Dans le gestionnaire d’autorisations, les destinataires de la stratégie d’autorisation sont représentés par les groupes suivants :

-   Utilisateurs et groupes Windows

    Ces groupes incluent les utilisateurs, les ordinateurs et les groupes intégrés pour les principaux de sécurité.

-   Groupes de requêtes LDAP

    L’appartenance à ces groupes est calculée dynamiquement en fonction des besoins à partir des requêtes LDAP (Lightweight Directory Access Protocol). Un groupe de requêtes LDAP est un type de groupe d’applications.

-   Groupes d’applications de base

    Ces groupes sont constitués de groupes de requêtes LDAP, d’utilisateurs et de groupes Windows et d’autres groupes d’applications de base.

## <a name="windows-users-and-groups"></a>Utilisateurs et groupes Windows

Ils sont les mêmes que les utilisateurs et les groupes utilisés dans le système d’exploitation Windows.

## <a name="ldap-query-groups"></a>Groupes de requêtes LDAP

Dans le gestionnaire d’autorisations, vous pouvez utiliser des requêtes LDAP pour faire correspondre les attributs de l’utilisateur avec ceux de l’objet de l’utilisateur dans Active Directory.

Par exemple, la requête suivante recherche tout le monde sauf Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



La requête suivante recherche tous les membres de l’alias de l’utilisateur sur www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Groupes d’applications de base

Dans l’API du gestionnaire d’autorisations, un groupe d’applications est représenté par un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) . Un groupe d’applications de base est un type de groupe d’applications.

Pour définir l’appartenance à un groupe d’applications de base, définissez qui est membre et définissez qui n’est pas membre. Ces deux étapes sont effectuées de la même façon. Spécifiez zéro, un ou plusieurs utilisateurs et groupes Windows, des groupes d’applications de base ou des groupes de requêtes LDAP définis précédemment. L’appartenance du groupe d’applications de base est calculée en supprimant tous les non-membres du groupe. Le gestionnaire d’autorisations le fait automatiquement au moment de l’exécution.

La non-appartenance à un groupe d’applications de base est prioritaire sur l’appartenance.

Les définitions d’appartenance circulaire ne sont pas autorisées ; ils génèrent le message d’erreur suivant : «impossible d’ajouter GroupName. Le problème suivant s’est produit : une boucle a été détectée.»

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de groupes d’utilisateurs en C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 




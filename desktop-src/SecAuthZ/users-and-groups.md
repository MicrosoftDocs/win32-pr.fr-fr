---
description: Explique la définition des utilisateurs et des groupes dans l’API du gestionnaire d’autorisations.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Utilisateurs et groupes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7d6ae84dba833ddd06eb81944cecb9aa401c0f8f1971c3164317cefae14fbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906819"
---
# <a name="users-and-groups"></a>Utilisateurs et groupes

Dans le gestionnaire d’autorisations, les destinataires de la stratégie d’autorisation sont représentés par les groupes suivants :

-   Windows Utilisateurs et groupes

    Ces groupes incluent les utilisateurs, les ordinateurs et les groupes intégrés pour les principaux de sécurité.

-   Groupes de requêtes LDAP

    L’appartenance à ces groupes est calculée dynamiquement en fonction des besoins à partir des requêtes LDAP (Lightweight Directory Access Protocol). Un groupe de requêtes LDAP est un type de groupe d’applications.

-   Groupes d’applications de base

    ces groupes se composent de groupes de requêtes LDAP, Windows des utilisateurs et des groupes, et d’autres groupes d’applications de base.

## <a name="windows-users-and-groups"></a>Windows Utilisateurs et groupes

ils sont identiques aux utilisateurs et aux groupes utilisés dans le système d’exploitation Windows.

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

Pour définir l’appartenance à un groupe d’applications de base, définissez qui est membre et définissez qui n’est pas membre. Ces deux étapes sont effectuées de la même façon. spécifiez zéro, un ou plusieurs Windows utilisateurs et groupes, des groupes d’applications de base définis précédemment ou des groupes de requêtes LDAP. L’appartenance du groupe d’applications de base est calculée en supprimant tous les non-membres du groupe. Le gestionnaire d’autorisations le fait automatiquement au moment de l’exécution.

La non-appartenance à un groupe d’applications de base est prioritaire sur l’appartenance.

Les définitions d’appartenance circulaire ne sont pas autorisées ; ils génèrent le message d’erreur suivant : «impossible d’ajouter GroupName. Le problème suivant s’est produit : une boucle a été détectée.»

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de groupes d’utilisateurs en C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 




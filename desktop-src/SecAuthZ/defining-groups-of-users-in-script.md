---
description: Un objet IAzApplicationGroup représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective. Un objet IAzApplicationGroup peut également inclure d’autres objets IAzApplicationGroup en tant que membres.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Définition de groupes d’utilisateurs dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320550"
---
# <a name="defining-groups-of-users-in-script"></a>Définition de groupes d’utilisateurs dans le script

Dans le gestionnaire d’autorisations, un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective. Un objet **IAzApplicationGroup** peut également inclure d’autres objets **IAzApplicationGroup** en tant que membres. Pour plus d’informations sur les groupes d’applications, voir [utilisateurs et groupes](users-and-groups.md).

Un groupe peut être défini à l’aide de listes explicites de membres et de non-membres ou d’une requête LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ). Les exemples suivants montrent comment créer chaque type de groupe d’applications :

-   [Création d’un groupe de base](#creating-a-basic-group)
-   [Création d’un groupe de requêtes LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Création d’un groupe de base

Un groupe d’applications de base est défini par les membres inclus dans les propriétés des [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) et des non- [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) de l’objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) qui représente le groupe. Les utilisateurs et les groupes répertoriés dans la propriété **membres** sont inclus dans le groupe d’applications, et les utilisateurs et les groupes répertoriés dans la propriété non- **membres** sont exclus du groupe d’applications. La liste de la propriété des éléments qui n’est pas **membre** est remplacée par la liste dans la propriété **members** .

L’exemple suivant montre comment créer un groupe d’applications de base et ajouter tous les utilisateurs locaux en tant que membres de ce groupe. L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Création d’un groupe de requêtes LDAP

Un groupe de requêtes LDAP a une appartenance définie par la requête contenue dans la valeur de sa propriété [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .

L’exemple suivant montre comment créer un groupe d’applications de requête LDAP et ajouter tous les utilisateurs en tant que membres de ce groupe. L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 

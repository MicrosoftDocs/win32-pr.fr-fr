---
description: Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Création d’un objet du magasin de stratégies d’autorisation dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096077"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Création d’un objet du magasin de stratégies d’autorisation dans le script

Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications. Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin. Lorsqu’une application qui utilise le gestionnaire d’autorisations initialise, elle charge ces informations à partir du magasin. Le magasin de stratégies d’autorisation doit se trouver sur un système approuvé, car les administrateurs de ce système disposent d’un haut niveau d’accès au magasin.

Le gestionnaire d’autorisations prend en charge le stockage de la stratégie d’autorisation dans le service d’annuaire Active Directory ou dans un fichier XML, comme indiqué dans les exemples suivants. Dans l’API du gestionnaire d’autorisations, un magasin de stratégies d’autorisation est représenté par un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Les exemples montrent comment créer un objet **AzAuthorizationStore** pour un magasin de Active Directory et un magasin XML.

-   [Création d’un magasin de Active Directory](#creating-an-active-directory-store)
-   [création d’un magasin de SQL Server](#creating-a-sql-server-store)
-   [Création d’un magasin XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Création d’un magasin de Active Directory

pour utiliser Active Directory pour stocker la stratégie d’autorisation, le domaine doit être au niveau fonctionnel du domaine **Windows Server 2003** . Le magasin de stratégies d’autorisation ne peut pas être situé dans un **contexte d’attribution de noms sans domaine** (également appelé partition d’application). Il est recommandé de placer le magasin dans le conteneur de **données de programme** sous une nouvelle unité d’organisation créée spécifiquement pour le magasin de stratégies d’autorisation. Il est également recommandé de placer le magasin dans le même réseau local que les serveurs d’applications qui exécutent des applications qui utilisent le Windows Store.

L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans Active Directory. L’exemple suppose qu’il existe déjà une Active Directory unité d’organisation nommée Program Data dans un domaine nommé authmanager.com.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a>création d’un magasin de SQL Server

le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation basé sur Microsoft SQL Server. pour créer un magasin d’autorisations basé sur SQL Server, utilisez une URL qui commence par le préfixe **MSSQL://**. l’URL doit contenir une chaîne de connexion SQL valide, un nom de base de données et le nom du magasin de stratégies d’autorisation : **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

si l’instance de SQL Server ne contient pas la base de données du gestionnaire d’autorisations spécifiée, le gestionnaire d’autorisations crée une nouvelle base de données portant ce nom.

> [!Note]  
> les connexions à un magasin de SQL Server ne sont pas chiffrées, sauf si vous configurez explicitement SQL le chiffrement pour la connexion ou configurez le chiffrement du trafic réseau qui utilise le protocole IPsec (Internet Protocol Security).

 

l’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans une base de données SQL Server.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a>Création d’un magasin XML

Le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation au format XML. Le magasin XML peut se trouver sur le même ordinateur que celui où l’application s’exécute, ou il peut être stocké à distance. La modification directe du fichier XML n’est pas prise en charge. Utilisez le composant logiciel enfichable MMC du gestionnaire d’autorisations ou l’API du gestionnaire d’autorisations pour modifier le magasin de stratégies.

Le gestionnaire d’autorisations ne prend pas en charge la délégation de l’administration d’un magasin de stratégies XML. Pour plus d’informations sur la délégation, consultez délégation [de la définition des autorisations dans le script](delegating-the-defining-of-permissions-in-script.md).

L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans un fichier XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 




---
description: Vous pouvez déléguer l’administration des magasins de stratégies d’autorisation stockés dans Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Délégation de la définition des autorisations dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69cf0793a48a572ec4b37cbf3634f65b04ff3565f3205bf0380c68914abb4530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782063"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Délégation de la définition des autorisations dans le script

Vous pouvez déléguer l’administration des magasins de stratégies d’autorisation stockés dans Active Directory. L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue.

À chaque niveau correspond une liste d’administrateurs et de lecteurs. Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué. Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.

Un utilisateur ou un groupe qui est soit un administrateur, soit un lecteur d’une application doit également être ajouté en tant qu’utilisateur délégué du magasin de stratégies qui contient cette application. De même, un utilisateur ou un groupe qui est un administrateur ou un lecteur d’étendue doit être ajouté en tant qu’utilisateur délégué de l’application qui contient cette étendue.

**Pour déléguer l’administration d’une étendue**

1.  Ajoutez l’utilisateur ou le groupe à la liste des utilisateurs délégués du magasin qui contient l’étendue en appelant la méthode [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) de l’objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui contient l’étendue.
2.  Ajoutez l’utilisateur ou le groupe à la liste des utilisateurs délégués de l’application qui contient l’étendue en appelant la méthode [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) de l’objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui contient l’étendue.
3.  Ajoutez l’utilisateur ou le groupe à la liste des administrateurs de l’étendue en appelant la méthode [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) de l’objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .

> [!Note]  
> Les magasins de stratégies basés sur XML ne prennent pas en charge la délégation à un niveau quelconque.

 

Si une étendue dans un magasin d’autorisations qui est stocké dans Active Directory contient des définitions de tâches qui incluent des règles d’autorisation ou des définitions de rôles qui incluent des règles d’autorisation, l’étendue ne peut pas être déléguée.

L’exemple suivant montre comment déléguer l’administration d’une application. L’exemple suppose qu’il existe déjà un magasin de stratégies d’autorisation Active Directory à l’emplacement spécifié, que ce magasin de stratégies contient une application nommée Expense et que cette application ne contient pas de tâches avec des scripts de règle d’entreprise.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 




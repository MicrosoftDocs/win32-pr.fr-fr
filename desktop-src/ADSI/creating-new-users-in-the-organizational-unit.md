---
title: Création de nouveaux utilisateurs dans l’unité d’organisation
description: Terry Adams a été embauché dans l’organisation Fabrikam Sales. Son rapport direct est Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Création d’utilisateurs dans l’ADSI de l’unité d’organisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76d62c8d95e7d5e421fc562e38716477ff2dfb8f4097d4652710e2c50715487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180114"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Création de nouveaux utilisateurs dans l’unité d’organisation

Terry Adams a été embauché dans l’organisation Fabrikam Sales. Son rapport direct est Patrick Hines.

Comme indiqué dans l’exemple de code suivant, Joe Durand, administrateur d’entreprise, crée un compte pour lui.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



Lorsque vous créez un utilisateur, vous devez spécifier un **sAMAccountName**. Il s’agit d’un attribut obligatoire pour la classe utilisateur. Avant de pouvoir créer une instance d’un objet, vous devez définir tous les attributs obligatoires. Le **sAMAccountName** est généré automatiquement s’il n’est pas spécifié pour un nouvel utilisateur.

Lorsque vous créez un utilisateur, tous les attributs requis doivent être définis dans le cache local avant l’appel de la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Joe, en tant qu’administrateur, peut attribuer le mot de passe de Terry à l’aide de la méthode [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) . La méthode **IADsUser. SetPassword** ne fonctionnera pas tant que la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’a pas été appelée.

Joe active ensuite le compte d’utilisateur en affectant à la propriété [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) la **valeur false**.

L’exemple de code suivant montre comment définir Thierry comme responsable de Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Vous vous demandez peut-être ce qui se passe si Thierry change de nom, passe à une autre organisation ou quitte l’entreprise. Qui gère-t-il ce lien de rapport direct ? Pour plus d’informations et pour obtenir la solution à ce problème, consultez [réorganisation](reorganization.md). Étant donné que le schéma de Active Directory est extensible, vous pouvez modéliser vos objets de manière à inclure des relations de style gestionnaire-directe similaires.

Avant de passer à la tâche suivante, consultez un exemple de code qui montre comment Joe affichera les collaborateurs directs de Terry.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



Dans cet exemple de code, Patrick s’affiche comme le rapport direct de Terry, même si l’attribut **DirectReports** n’a jamais été modifié. Active Directory le fait automatiquement.

Dans le monde de l’annuaire, un attribut peut avoir une ou plusieurs valeurs. Comme **DirectReports** a plusieurs valeurs, vous pouvez accéder à ces informations en examinant le schéma, il est plus facile d’utiliser la méthode [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , qui retourne un tableau de valeurs, qu’une seule ou plusieurs valeurs soient retournées.

Le composant logiciel enfichable utilisateurs et ordinateurs Active Directory vous permet d’afficher les rapports directs et les relations du gestionnaire sur la page de propriétés de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout d’utilisateurs à un groupe](adding-users-to-a-group.md)
</dt> </dl>

 

 





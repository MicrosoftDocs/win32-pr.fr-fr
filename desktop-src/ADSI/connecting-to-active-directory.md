---
title: Connexion à Active Directory
description: Plusieurs méthodes sont utilisées pour accéder à Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Connexion à Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939601"
---
# <a name="connecting-to-active-directory"></a>Connexion à Active Directory

Plusieurs méthodes sont utilisées pour accéder à Active Directory. Il est recommandé d’utiliser l’API ADSI pour accéder à Active Directory. ADSI implémente le protocole LDAP pour communiquer avec Active Directory. Les exemples de code suivants montrent comment accéder à Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Cela ouvre le fournisseur LDAP et le prépare à la récupération des données. Aucune connexion n’est établie tant que les données ne sont pas demandées. Lorsque les données sont demandées, ADSI, avec l’aide du service Localisateur, tente de trouver le meilleur contrôleur de domaine pour la connexion et établit une connexion au serveur. Ce processus porte le nom de liaison sans serveur.

ADSI vous permet également de spécifier le nom du serveur à utiliser pour la connexion.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



Dans un autre scénario, vous pouvez uniquement connaître le nom de domaine, mais pas le nom de serveur spécifique. Là encore, ADSI vous permet de spécifier le nom de domaine. Dans Windows 2000, le nom de domaine est représenté sous la forme d’un nom DNS. Par exemple, si Joe worden, l’administrateur réseau, choisit de se connecter à l’aide du nom de domaine, il peut utiliser l’exemple de code suivant.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI se connectera à l’un des contrôleurs de domaine dans le domaine fabrikam.com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison à des objets Active Directory](binding-to-active-directory-objects.md)
</dt> </dl>

 

 





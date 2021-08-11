---
title: Déplacement des utilisateurs existants vers l’unité d’organisation
description: Lorsque l’administrateur d’entreprise, Joe worden, met à niveau le domaine Windows NT 4,0 vers Active Directory, tous les utilisateurs et les groupes sont migrés vers les conteneurs utilisateurs dans le domaine fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Déplacement des utilisateurs existants vers la publicité d’unité d’organisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178953"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Déplacement des utilisateurs existants vers l’unité d’organisation

Lorsque l’administrateur d’entreprise, Joe worden, met à niveau le domaine Windows NT 4,0 vers Active Directory, tous les utilisateurs et les groupes sont migrés vers les conteneurs utilisateurs dans le domaine fabrikam. Joe peut à présent déplacer ces utilisateurs et groupes vers les unités d’organisation appropriées. un objet peut également être déplacé entre les domaines Windows 2000 associés à l’aide d’ADSI.

Dans l’exemple de code suivant, Joe déplace « JeffSmith » vers l’organisation Sales.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



La méthode [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) prend l’ADsPath de l’objet à déplacer et le nouveau nom de l’objet (RDN). Pour conserver le même nom, vous pouvez spécifier **null** (**vbNullString**) pour le paramètre *bstrNewName* . Pour renommer l’objet lorsqu’il est déplacé, spécifiez le nouveau nom unique relatif pour le paramètre *bstrNewName* . Par exemple, pour déplacer JeffSmith vers l’organisation Sales et renommer l’objet « JeffSmith » en « Jeff \_ Smith » dans la même opération, Joe exécute le code suivant :


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de nouveaux utilisateurs dans l’unité d’organisation](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 





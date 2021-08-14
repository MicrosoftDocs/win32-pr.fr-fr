---
title: Ajout d’utilisateurs à un groupe
description: Joe worden, administrateur d’entreprise, ajoutera désormais Julie Bankert au groupe d’administration. Pour ajouter un objet à un groupe, utilisez la méthode IADsGroup. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Ajout d’utilisateurs à un groupe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607c9b5ae68056293d4b57f2b5d1937d79de2fd3019747afd6add922ca3c6937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181170"
---
# <a name="adding-users-to-a-group"></a>Ajout d’utilisateurs à un groupe

Joe worden, administrateur d’entreprise, ajoutera désormais Julie Bankert au groupe d’administration. Pour ajouter un objet à un groupe, utilisez la méthode [**IADsGroup. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un nouveau groupe](creating-a-new-group.md)
</dt> </dl>

 

 





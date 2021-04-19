---
title: Méthode GetEx
description: Certains attributs peuvent stocker une ou plusieurs valeurs.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, utilisation de IADs GetEx
- ADSI ADSI, utilisation de, à l’aide de la méthode IADs GetEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508955"
---
# <a name="the-getex-method"></a>Méthode GetEx

Certains attributs peuvent stocker une ou plusieurs valeurs. Par exemple, l’attribut **OtherTelephone** d’un objet utilisateur dans Active Directory est une propriété qui peut avoir zéro, une ou plusieurs valeurs. Les attributs qui ont plusieurs valeurs sont appelés « attributs à valeurs multiples ». Si la méthode [**IADs :: obten**](/windows/desktop/api/Iads/nf-iads-iads-get) est utilisée pour récupérer un attribut à valeurs multiples, les résultats doivent être traités différemment que si l’attribut a une seule valeur. Toutefois, les résultats fournis par la méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sont traités de la même manière, que l’attribut ait une ou plusieurs valeurs. Dans les deux cas, la méthode **IADs :: GETEX** retourne les valeurs dans un tableau.

La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) récupère les propriétés du cache de propriétés. Si la propriété spécifiée est introuvable dans le cache, **IADs :: GETEX** effectue un appel [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicite.

La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retourne un tableau de variants de variantes, quel que soit le nombre de valeurs retournées par le serveur. Cela est vrai même si l’attribut ne contient qu’une seule valeur.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) peut également être utilisée pour les attributs à valeur unique. Les résultats d’un attribut à valeur unique sont traités de la même façon que les résultats d’un attribut à valeurs multiples.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Si aucune valeur n’est définie pour l’attribut, [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retourne l’erreur « la propriété est introuvable dans le cache ».

 

 





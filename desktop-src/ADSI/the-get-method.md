---
title: Méthode d’extraction
description: La méthode d’extraction IADs est utilisée pour récupérer des attributs nommés individuels d’un objet d’annuaire.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Procurez-vous ADSI en utilisant les IAD
- ADSI ADSI, utilisation de, à l’aide de la méthode d’extraction IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512632"
---
# <a name="the-get-method"></a>Méthode d’extraction

La méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) permet de récupérer des attributs nommés individuels à partir d’un objet d’annuaire.

L’exemple de code suivant utilise la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) pour récupérer un attribut nommé à partir d’un objet.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Dans les langages d’automatisation, il est également possible d’accéder directement aux attributs nommés à l’aide de la notation par points. Par exemple, **objet. La valeur de l’objet obtient (« distinguishedName »)** est identique à **Object. DistinguishedName**.

L’exemple de code suivant est identique à l’exemple précédent, à ceci près que l’attribut **distinguishedName** est accessible à l’aide de la notation par points.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Si aucune valeur n’est définie pour l’objet, la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) retourne l’erreur « la propriété est introuvable dans le cache ».

 

 





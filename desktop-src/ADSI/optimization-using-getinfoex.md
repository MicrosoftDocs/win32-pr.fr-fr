---
title: Optimisation à l’aide de GetInfoEx
description: Utilisé pour charger des valeurs d’attribut spécifiques dans le cache local à partir du service d’annuaire sous-jacent.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimisation à l’aide d’ADSI GetInfoEx
- GetInfoEx ADSI, optimisation à l’aide d’IADs GetInfoEx
- ADSI ADSI, utilisation, optimisation à l’aide de la méthode IADs GetInfoEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316452"
---
# <a name="optimization-using-getinfoex"></a>Optimisation à l’aide de GetInfoEx

La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) est utilisée pour charger des valeurs d’attribut spécifiques dans le cache local à partir du service d’annuaire sous-jacent. Cette méthode charge uniquement les valeurs d’attribut spécifiées dans le cache local. La méthode [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) permet de charger toutes les valeurs d’attribut dans le cache local.

La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtient des valeurs actuelles spécifiques pour les propriétés d’un objet Active Directory à partir du magasin d’annuaires sous-jacent, en actualisant les valeurs mises en cache.

Toutefois, si une valeur existe déjà dans le cache de propriétés, l’appel de la méthode [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sans appeler d’abord les [**IAD. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour cet attribut récupérera la valeur mise en cache plutôt que la valeur la plus récente de l’annuaire sous-jacent. Cela peut entraîner le remplacement des valeurs d’attribut mises à jour si le cache local a été modifié, mais que les valeurs n’ont pas été validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . La méthode suggérée pour éviter les problèmes de mise en cache consiste à toujours valider les modifications de valeur d’attribut en appelant **IADs. setinfo** avant d’appeler [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Récupération des attributs construits Active Directory

Dans Active Directory, la plupart des attributs construits sont récupérés et mis en cache quand la méthode [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) est appelée ([**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) effectue un appel de **IADs. GetInfo** implicite si le cache est vide). Certains attributs construits, toutefois, ne sont pas automatiquement récupérés et mis en cache et nécessitent donc que la méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) soit appelée explicitement pour les récupérer. Par exemple, dans Active Directory, l’attribut [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) n’est pas récupéré lorsque la méthode **IADs. GetInfo** est appelée et les **IAD. obtenir** renvoient la **\_ propriété E ADS \_ \_ \_ introuvable**. La méthode **IADs. GetInfoEx** doit être appelée pour récupérer l’attribut **canonicalName** . Ces mêmes attributs construits ne seront pas non plus extraits à l’aide de l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) pour énumérer les attributs.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment récupérer toutes les valeurs d’attribut, consultez l' [exemple de code pour la lecture d’un attribut construit](example-code-for-reading-a-constructed-attribute.md).

 

 
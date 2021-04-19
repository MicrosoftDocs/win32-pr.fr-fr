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
# <a name="the-get-method"></a><span data-ttu-id="80e3c-105">Méthode d’extraction</span><span class="sxs-lookup"><span data-stu-id="80e3c-105">The Get Method</span></span>

<span data-ttu-id="80e3c-106">La méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) permet de récupérer des attributs nommés individuels à partir d’un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="80e3c-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="80e3c-107">L’exemple de code suivant utilise la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) pour récupérer un attribut nommé à partir d’un objet.</span><span class="sxs-lookup"><span data-stu-id="80e3c-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


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



<span data-ttu-id="80e3c-108">Dans les langages d’automatisation, il est également possible d’accéder directement aux attributs nommés à l’aide de la notation par points.</span><span class="sxs-lookup"><span data-stu-id="80e3c-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="80e3c-109">Par exemple, **objet. La valeur de l’objet obtient (« distinguishedName »)** est identique à **Object. DistinguishedName**.</span><span class="sxs-lookup"><span data-stu-id="80e3c-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="80e3c-110">L’exemple de code suivant est identique à l’exemple précédent, à ceci près que l’attribut **distinguishedName** est accessible à l’aide de la notation par points.</span><span class="sxs-lookup"><span data-stu-id="80e3c-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


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



<span data-ttu-id="80e3c-111">Si aucune valeur n’est définie pour l’objet, la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) retourne l’erreur « la propriété est introuvable dans le cache ».</span><span class="sxs-lookup"><span data-stu-id="80e3c-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 





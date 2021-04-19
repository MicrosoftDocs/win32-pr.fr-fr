---
title: Délégation d’unités d’organisation
description: La société Fabrikam engage deux administrateurs, Mike et Paul, à gérer les unités d’organisation est et ouest, respectivement.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510388"
---
# <a name="delegating-organizational-units"></a>Délégation d’unités d’organisation

La société Fabrikam engage deux administrateurs, Mike et Paul, à gérer les unités d’organisation est et ouest, respectivement. Jean délègue ses responsabilités administratives pour qu’il puisse créer et supprimer des utilisateurs dans leurs unités d’organisation respectives.

Avant de voir comment configurer ces unités d’organisation sous Mike et Paul, vous devez comprendre comment configurer l’accès aux objets dans Active Directory. Chaque objet dans Active Directory possède un descripteur de sécurité. Avec le descripteur de sécurité, vous pouvez modifier les autorisations sur l’objet, propager les autorisations, activer l’audit, et ainsi de suite. Le descripteur de sécurité a lui-même deux listes de contrôle d’accès (ACL) : une liste ACL discrétionnaire (DACL) et une ACL système (SACL). Chaque liste ACL peut contenir des entrées de contrôle d’accès (ACE). Avec une entrée du contrôle d’accès, vous pouvez définir l’accès autorisé ou refusé sur un objet. En outre, vous pouvez spécifier des actions spécifiques à autoriser ou refuser. Voici quelques exemples d’actions : créer un enfant, supprimer un enfant, lire la propriété et écrire la propriété. Ces droits sont spécifiés avec [**AccessMask**](iadsaccesscontrolentry-property-methods.md).

Ensuite, vous pouvez spécifier les classes ou les attributs auxquels cette entrée du contrôle d’accès (ACE) est associée. Dans l’exemple Fabrikam qui suit, Joe choisit la classe utilisateur afin que chaque administrateur puisse ajouter des utilisateurs au système. Ensuite, vous devez répondre à la question suivante : « qui sera le bénéficiaire de cette entrée de contrôle d’accès ? » Joe spécifie Mike.

Enfin, vous pouvez définir le comportement d’héritage de l’entrée du contrôle d’accès. par exemple, les entrées de contrôle d’accès peuvent être spécifiées pour se propager dans la hiérarchie. En résumé, l’exemple précédent donne à Mike la possibilité de créer et de supprimer des objets utilisateur sous l’unité d’organisation East Sales.

Joe utilise l’exemple de code suivant pour configurer les ACE et les listes de contrôle d’accès sur l’unité d’organisation East.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



L’illustration suivante montre le menu Active Directory **créer une nouvelle vue** après l’exécution du code. Quand Jean, l’administrateur ouvre une session, il voit plusieurs classes qu’il peut créer. Toutefois, lorsque Mike ouvre une session, il peut uniquement créer des objets utilisateur.

![menu créer une option de vue](images/adadsi5.png)

Pour plus d’informations, consultez [modèle de sécurité ADSI](adsi-security-model.md).

 

 





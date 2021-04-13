---
title: Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects
description: Les objets de la classe de conteneur ont un attribut otherWellKnownObjects que vous pouvez utiliser pour associer un GUID au nom unique (DN) d’un objet enfant dans le conteneur.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propriété otherWellKnownObjects
- propriété otherWellKnownObjects, à l’aide de pour une liaison de renommage sécurisée
- Active Directory, utilisation de, liaison, liaison de renommage sécurisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190770"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects

Les objets de la classe de conteneur ont un attribut **otherWellKnownObjects** que vous pouvez utiliser pour associer un GUID au nom unique (DN) d’un objet enfant dans le conteneur. Si l’objet enfant est déplacé ou renommé, le serveur Active Directory met à jour le DN dans la valeur **otherWellKnownObjects** de cet objet enfant. Cela permet d’utiliser la fonctionnalité de liaison WKGUID pour établir une liaison à l’objet enfant à l’aide du GUID et du DN du conteneur plutôt que du DN de l’objet enfant.

L’attribut **otherWellKnownObjects** est équivalent à l’attribut **wellKnownObjects** , à ceci près que les applications et services peuvent écrire une valeur **otherWellKnownObjects** , mais que seul le système peut écrire **wellKnownObjects**.

L’utilisation de l’attribut **otherWellKnownObjects** et de la liaison WKGUID est bénéfique dans les cas suivants où la liaison de renommage sécurisée est requise par rapport à un objet conteneur spécifique.

Si un objet conteneur contient d’autres objets importants ou si des objets importants peuvent être renommés ou déplacés.

Si les objets importants existent pour chaque instance de l’objet conteneur. Par exemple, le système utilise l’attribut **wellKnownObjects** de chaque objet **domainDNS** pour stocker une valeur pour le conteneur Users, qui existe dans chaque instance d’un objet **domainDNS** . Cela permet aux applications de se lier au conteneur Users de manière sécurisée en spécifiant le GUID connu et le DN du conteneur **domainDNS** . Les applications peuvent utiliser l’attribut **otherWellKnownObjects** d’un conteneur de la même façon.

Si vous avez besoin d’une liaison et/ou d’une fonctionnalité de recherche de renommage sécurisé sur les objets importants.

**Pour ajouter des fonctionnalités de recherche et de liaison avec renommage sécurisé**

1.  Ajoutez une valeur à la propriété **otherWellKnownObjects** de l’objet conteneur lorsque l’objet important est créé dans ce conteneur. La valeur contient le GUID qui représente l’objet connu. N’oubliez pas qu’il ne s’agit pas de l' **objectGUID** et du **distinguishedName** pour cet objet.
2.  Utilisez la fonctionnalité de liaison WKGUID pour effectuer une liaison ou une recherche dans l’objet important.

L’attribut **otherWellKnownObjects** peut avoir plusieurs valeurs et contient les tuples GUID/DN des objets connus dans les conteneurs sur lesquels ils sont définis. L’attribut **otherWellKnownObjects** a la syntaxe DNWithBinary dans laquelle les valeurs se présentent sous la forme suivante :


```C++
B:<char count>:<well known GUID>:<object DN>
```



Dans cet exemple, « &lt; nombre &gt; de caractères » est le nombre de chiffres hexadécimaux dans « &lt; GUID connu &gt; », qui est 32 (nombre de chiffres hexadécimaux dans un GUID) pour **otherWellKnownObjects** et **wellKnownObjects**. « &lt; GUID connu &gt; » est la représentation de chiffres hexadécimaux du GUID connu. « &lt; Object DN &gt; » est le nom unique de l’objet représenté par cette valeur WKO. Le serveur gère la partie ObjectDN de chaque valeur **wellKnownObjects** et **otherWellKnownObjects** afin qu’il contienne le nom unique actuel de l’objet spécifié à l’origine lors de la création de la valeur.

Par exemple, si {df447b5e-AA5B-11D2-8D53-00c04f79ab81} est le GUID connu de l’objet MyObject dans le conteneur MyContainer du domaine Fabrikam.com, la valeur **otherWellKnownObjects** spécifie le GUID connu et le DN de MyObject :


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Pour effectuer une liaison à cet objet, utilisez la chaîne de liaison WKGUID suivante qui spécifie le GUID connu de l’objet et le DN du conteneur :


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Après la liaison à cet objet, vous pouvez utiliser les interfaces COM ADSI pour rechercher, lire, modifier ou supprimer l’objet.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment ajouter un objet à l’attribut **otherWellKnownObjects** , consultez l' [exemple de code pour la création d’un objet conteneur](example-code-for-creating-a-container-object.md).

 

 





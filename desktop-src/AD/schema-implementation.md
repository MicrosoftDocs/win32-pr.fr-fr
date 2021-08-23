---
title: Implémentation du schéma
description: Dans Active Directory Domain Services, les définitions de classe et d’attribut sont stockées dans le répertoire en tant qu’instances des classes classSchema et attributeSchema, respectivement.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025017"
---
# <a name="schema-implementation"></a>Implémentation du schéma

Dans Active Directory Domain Services, les définitions de classe et d’attribut sont stockées dans le répertoire en tant qu’instances des classes [**classSchema**](/windows/desktop/ADSchema/c-classschema) et [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) , respectivement. **classSchema** et **attributeSchema** sont des classes définies dans le schéma. Pour manipuler le schéma Active Directory, utilisez les mêmes opérations LDAP utilisées pour manipuler un autre objet. Étant donné que le schéma est une partie essentielle du répertoire qui affecte l’ensemble de la forêt, des restrictions spéciales s’appliquent aux extensions de schéma. Pour plus d’informations sur les restrictions, consultez [restrictions sur les extensions de schéma](restrictions-on-schema-extension.md).

Pour résumer l’implémentation du schéma :

-   Les instances de la classe [**classSchema**](/windows/desktop/ADSchema/c-classschema) définissent chaque classe d’objet prise en charge par Active Directory Domain Services. Les attributs d’un objet **classSchema** , par exemple, ses [**attributs mayContain**](/windows/desktop/ADSchema/a-maycontain) et [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) , décrivent une classe d’objet, de la même façon que les attributs d’un objet utilisateur, par exemple, ses attributs [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) et [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) , décrivent cet utilisateur. Pour plus d’informations, consultez [caractéristiques des classes d’objets](characteristics-of-object-classes.md).
-   Les instances de la classe [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) sont utilisées pour définir chaque attribut pris en charge par Active Directory Domain Services. Les attributs d’un objet **attributeSchema** , par exemple, ses attributs **attributeSyntax** et **isSingleValued** , décrivent un attribut, de la même façon que les attributs d’un objet utilisateur décrivent cet utilisateur. Pour plus d’informations, consultez [caractéristiques des attributs](characteristics-of-attributes.md).
-   Les instances des classes [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) et [**classSchema**](/windows/desktop/ADSchema/c-classschema) sont stockées dans un emplacement bien connu dans l’annuaire, le conteneur de schéma. Le conteneur de schéma a toujours un nom unique de la forme :

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    où « &lt; DC = forestroot &gt; » est le nom unique de la racine de la forêt, par exemple, « DC = fabrikam, DC = com ».

    Pour obtenir le nom unique du conteneur de schéma, lisez l’attribut **schemaNamingContext** de rootDSE. Pour plus d’informations sur rootDSE et ses attributs, consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).

Lorsque vous réfléchissez au schéma, n’oubliez pas :

-   Les modifications de schéma sont globales. Il existe un seul schéma pour une forêt entière. Le schéma est répliqué à l’échelle mondiale : il existe une copie du schéma sur chaque contrôleur de domaine de la forêt. Lorsque vous étendez le schéma, vous le faites pour l’ensemble de la forêt.
-   Les ajouts de schéma ne sont pas réversibles. Lorsqu’une nouvelle classe ou un nouvel attribut est ajouté au schéma, il ne peut pas être supprimé. Un attribut ou une classe existant peut être désactivé, mais pas supprimé. Pour plus d’informations, consultez [désactivation des classes et attributs existants](disabling-existing-classes-and-attributes.md).
-   La désactivation d’une classe ou d’un attribut n’affecte pas les instances existantes de la classe ou de l’attribut, mais empêche la création de nouvelles instances. Vous ne pouvez pas désactiver un attribut s’il est inclus dans une classe qui n’est pas désactivée.

 

 
---
title: Impact des modifications de schéma
description: Cette rubrique décrit comment une extension de schéma a un impact sur la forêt Active Directory.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impact des modifications de schéma AD
- Active Directory de schéma, impact de la modification du schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509778"
---
# <a name="impact-of-schema-changes"></a>Impact des modifications de schéma

Une extension de schéma a un impact sur une forêt de domaine contrôlée par Active Directory Domain Services de plusieurs façons :

-   Les modifications de schéma sont globales. Il existe un seul schéma pour une forêt entière. Le schéma est répliqué à l’échelle mondiale : il existe une copie du schéma sur chaque contrôleur de groupe de la forêt. Lorsque vous étendez le schéma, il est étendu pour l’ensemble de la forêt.
-   Les ajouts d’objets de schéma ne peuvent pas être inversés. Lorsqu’un nouvel objet de classe ou d’attribut est ajouté au schéma, il ne peut pas être supprimé. Un attribut ou une classe existant peut être désactivé, mais pas supprimé. Pour plus d’informations, consultez [désactivation des classes et attributs existants](disabling-existing-classes-and-attributes.md). La désactivation d’une classe ou d’un attribut n’affecte pas les instances existantes de la classe ou de l’attribut, mais empêche la création de nouvelles instances. Vous ne pouvez pas désactiver un attribut s’il est inclus dans une classe qui n’est pas désactivée.
-   Les OID doivent être uniques. Lorsqu’un attribut ou une classe est ajouté au schéma, aucun attribut ou classe avec le même OID ne peut être ajouté. Cela est vrai même si une classe ou un attribut a été désactivé. Pour cette raison, vous devez utiliser des OID valides. Ne pas synthétiser un OID et ne pas réutiliser un OID existant. Pour plus d’informations sur l’obtention d’un OID valide, consultez [obtention d’un identificateur d’objet racine](obtaining-an-object-identifier.md).
-   Certaines modifications peuvent être apportées après la création :

    -   Pour une classe de catégorie 1 ou 2, vous pouvez ajouter ou supprimer des valeurs dans l’attribut **possSuperiors** . Les valeurs **possSuperiors** spécifient les classes d’objets qui peuvent contenir la classe.
    -   Pour une classe de catégorie 1 ou 2, vous pouvez ajouter ou supprimer des valeurs dans l’attribut **mayContain** . Les valeurs **mayContain** spécifient les attributs facultatifs, mais peuvent être présents dans une instance de la classe.

-   Le **lDAPDisplayName** pour une classe ou un attribut de catégorie 2 peut être modifié une fois qu’il a été créé. En règle générale, vous ne devez pas modifier le **lDAPDisplayName**. Toutefois, il existe une raison légitime de modifier le nom LDAP et c’est le cas si vous avez commis une erreur lors de la définition de l’attribut ou de la classe et que vous devez en créer un nouveau pour remplacer l’ancien. Pour ce faire, il n’est pas nécessaire de renommer le RDN (relative Distinguished Name) du schéma de la classe ou de l’attribut. Lorsque le nom LDAP est modifié, cela vous permet de contourner une erreur plutôt que de recréer l’ensemble de votre infrastructure Windows 2000. Pour plus d’informations, consultez [désactivation des classes et attributs existants](disabling-existing-classes-and-attributes.md).

    Le **lDAPDisplayName** des classes ou attributs prédéfinis (catégorie 1) ne peut pas être modifié. Pour plus d’informations sur les objets de schéma de catégorie 1 et 2, consultez [restrictions sur l’extension de schéma](restrictions-on-schema-extension.md).

 

 





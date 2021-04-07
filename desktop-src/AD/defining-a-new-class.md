---
title: Définition d’une nouvelle classe
description: Quand vous définissez une nouvelle classe, spécifiez les classes parentes juridiques de la nouvelle classe, autrement dit, les classes qui peuvent contenir des instances de votre nouvelle classe.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939650"
---
# <a name="defining-a-new-class"></a>Définition d’une nouvelle classe

Quand vous définissez une nouvelle classe, spécifiez les classes parentes juridiques de la nouvelle classe, autrement dit, les classes qui peuvent contenir des instances de votre nouvelle classe. Les classes parentes juridiques sont spécifiées dans les attributs **possSuperiors** et **systemPossSuperiors** de la nouvelle classe, ainsi que dans les supérieurs possibles hérités de ses superclasses, mais pas à partir des classes auxiliaires.

Être spécifique lors de la définition des classes parentes juridiques pour la nouvelle classe. Décidez où vous souhaitez que les utilisateurs créent des instances de votre classe. Par exemple, si vous spécifiez « Container » comme parent légal, l’utilisateur crée des instances sous l’un des conteneurs standard (**Container**, **OrganizationalUnit**, etc.), tandis que la spécification de « Computer » permet de créer des instances uniquement sous les instances de l’objet **ordinateur** .

**Pour créer une classe**

1.  Choisissez un nom pour la classe. Pour plus d’informations sur la composition d’un nom commun et d’un nom complet LDAP pour une nouvelle classe, consultez [Naming Attributes and classes](naming-attributes-and-classes.md).
2.  Obtenez un identificateur d’objet (OID) pour la classe. Pour plus d’informations, consultez [obtention d’un identificateur d’objet](obtaining-an-object-identifier.md).
3.  Choisissez une « catégorie d’objet par défaut » pour la classe. Pour plus d’informations, consultez [classe d’objet et catégorie d’objet](object-class-and-object-category.md).
4.  Choisissez une « catégorie de classe d’objet » pour la classe. Cela indique si la classe est abstraite, structurelle ou auxiliaire. Pour plus d’informations, consultez [classes structurelles, abstraites et auxiliaires](structural-abstract-and-auxiliary-classes.md).
5.  Créez un nouvel objet **classSchema** . De nombreux attributs peuvent être définis pour un objet **classSchema** . Les attributs suivants sont essentiels pour la définition d’une nouvelle classe :

    -   Classes dont hérite la nouvelle classe : **subClassOf**, **auxiliaryClass** et **systemAuxiliaryClass**
    -   Noms et identificateurs de la nouvelle classe : **CN**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**
    -   Attributs possibles de la nouvelle classe : **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**
    -   Parents possibles de la nouvelle classe : **possSuperiors**, **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **Description** (facultatif)

    Pour plus d’informations et pour obtenir une description de ces attributs, consultez [caractéristiques des classes d’objets](characteristics-of-object-classes.md).

    Sachez que les classes spécifiées dans **subClassOf**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass** et **systemAuxiliaryClass** doivent exister lorsque la nouvelle classe est écrite dans le répertoire ; dans le cas contraire, l’objet **classSchema** ne pourra pas être ajouté à l’annuaire. De même, les attributs spécifiés dans **mustContain**, **systemMustContain**, **mayContain** et **systemMayContain** doivent exister, sinon l’opération de création de la classe échouera.

6.  Écrivez le nouvel objet **classSchema** dans le répertoire.

**Pour ajouter un attribut à la propriété mayContain**

1.  Obtenez l’objet **classSchema** pour la classe à modifier.
2.  Ajoutez le nouvel attribut à la propriété à valeurs multiples **mayContain** .
3.  Réécrivez l’objet **classSchema** modifié dans le répertoire.

De nouveaux attributs peuvent être créés en même temps que de nouvelles classes ; l’ordre de création des nouveaux attributs et classes est important. Pour plus d’informations, consultez [ce que l’installation doit faire](what-the-installation-must-do.md).

**Pour ajouter de nouveaux attributs et de nouvelles classes en même temps**

1.  Définissez d’abord tous les nouveaux attributs. Pour plus d’informations, consultez [définition d’un nouvel attribut](defining-a-new-attribute.md).
2.  Mettez à jour le cache de schéma avant de définir de nouvelles classes. Pour plus d’informations, consultez [mise à jour du cache de schéma](updating-the-schema-cache.md).
3.  Créez les nouvelles classes.
4.  Ajoutez les attributs souhaités aux nouvelles classes.
5.  Mettez à jour le cache de schéma.

 

 





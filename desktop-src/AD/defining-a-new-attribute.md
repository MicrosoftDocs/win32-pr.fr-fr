---
title: Définition d’un nouvel attribut
description: Cette rubrique montre comment définir un nouvel attribut lors de l’extension du schéma Active Directory.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Définition d’une nouvelle publicité d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101460"
---
# <a name="defining-a-new-attribute"></a>Définition d’un nouvel attribut

Cette rubrique montre comment définir un nouvel attribut lors de l’extension du schéma Active Directory.

Tenez compte des éléments suivants lors de la définition d’un nouvel attribut :

-   Utilisez les attributs existants dans la mesure du possible.
-   Utilisez toujours la propriété **CN** (nom commun) comme attribut d’affectation de noms (nom unique relatif). Il s’agit de la valeur par défaut pour la plupart des classes, y compris celles dérivées directement du haut. La propriété **CN** est une propriété indexée qui rendra plus efficace la recherche d’objets par nom.
-   Les gros attributs à valeurs multiples sont coûteux à stocker et à récupérer et doivent être évités. Active Directory Domain Services implémenter une extension LDAP pour permettre la lecture incrémentielle des propriétés de grande taille avec plusieurs valeurs, mais tous les clients LDAP ne reconnaissent pas cette extension.
-   N’oubliez pas que les attributs sont plats, il n’existe pas de sous-structure implicite pour un attribut. Tous les attributs d’une classe donnée doivent être liés directement aux instances de cette classe.

## <a name="creating-a-new-attribute"></a>Création d’un nouvel attribut

Pour créer un nouvel attribut :

-   Choisissez un nom pour l’attribut. Le nom sera contenu dans les attributs **CN** et **lDAPDisplayName** . Pour plus d’informations sur la composition d’un nom pour un nouvel attribut, consultez Naming Attributes [and classes](naming-attributes-and-classes.md).
-   Obtenez un identificateur d’objet (OID) pour l’attribut. Pour plus d’informations, consultez [obtention d’un identificateur d’objet racine](obtaining-an-object-identifier.md).
-   Choisissez une syntaxe pour l’attribut. La syntaxe est déterminée par la combinaison des attributs **oMSyntax** et **oMObjectClass** . Pour plus d’informations, consultez [choix d’une syntaxe](choosing-a-syntax.md).
-   Déterminez si l’attribut est à valeur unique ou à valeurs multiples. L’attribut **isSingleValued** détermine si l’attribut est à valeur unique ou à valeurs multiples.
-   Déterminez si l’attribut doit être indexé par défaut. Pour plus d’informations, consultez [attributs indexés](indexed-attributes.md).
-   Déterminez si l’attribut doit figurer dans le catalogue global par défaut. Pour plus d’informations, consultez [attributs inclus dans le catalogue global](attributes-included-in-the-global-catalog.md).
-   Si l’attribut est un entier ou une chaîne, déterminez si une limite de plage est requise. Les attributs **rangeLower** et **rangeUpper** sont utilisés pour spécifier la limite de plage.
-   Si l’attribut est à valeur unique, déterminez si l’attribut doit être lié à un autre attribut. Dans ce cas, l’attribut [**LinkId**](/windows/desktop/ADSchema/a-linkid) doit être défini de manière appropriée sur chaque attribut ; un attribut doit être un lien suivant, l’autre un lien précédent. Pour plus d’informations sur les attributs liés, consultez [attributs liés](linked-attributes.md).
-   Créez un nouvel objet **attributeSchema** dans le conteneur de schéma et définissez les attributs appropriés pour l’objet. Un grand nombre d’attributs peuvent être définis pour un objet **attributeSchema** , mais les attributs répertoriés dans le tableau ci-dessous sont essentiels pour la définition d’un nouvel attribut. Les valeurs de ces attributs sont déterminées par les étapes précédentes. Pour plus d’informations sur ces attributs, consultez [caractéristiques des attributs](characteristics-of-attributes.md).

    | Attribut                                    | Commentaire                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **cn**<br/>                            | Obligatoire.<br/>                                 |
    | **lDAPDisplayName**<br/>               | Obligatoire.<br/>                                 |
    | **adminDisplayName**<br/>              | Obligatoire.<br/>                                 |
    | **attributeSyntax**<br/>               | Obligatoire.<br/>                                 |
    | **oMSyntax**<br/>                      | Obligatoire.<br/>                                 |
    | **oMObjectClass**<br/>                 | Obligatoire.<br/>                                 |
    | **schemaIDGUID**<br/>                  | Obligatoire.<br/>                                 |
    | **attributeID**<br/>                   | Obligatoire.<br/>                                 |
    | **isSingleValued**<br/>                | Obligatoire.<br/>                                 |
    | **searchFlags**<br/>                   | Obligatoire.<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | Obligatoire.<br/>                                 |
    | **rangeLower**<br/>                    | Optionnel.<br/>                                 |
    | **rangeUpper**<br/>                    | Optionnel.<br/>                                 |
    | **Égale**<br/>                        | Optionnel. Requis pour les attributs liés.<br/> |
    | **description**<br/>                   | Optionnel.<br/>                                 |

    

     

-   Validez le nouvel objet **attributeSchema** dans le conteneur de schéma.
-   Mettez à jour le cache de schéma, si nécessaire. Pour plus d’informations, consultez [mise à jour du cache de schéma](updating-the-schema-cache.md).

 


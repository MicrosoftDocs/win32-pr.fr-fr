---
title: Nommer des classes et des attributs
description: Cette rubrique contient des instructions pour nommer des attributs et des classes.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Nommer des classes et des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "106511110"
---
# <a name="naming-attributes-and-classes"></a>Nommer des classes et des attributs

Cette rubrique contient des instructions pour nommer des attributs et des classes.

Pour créer une classe ou un attribut, respectez les règles d’affectation de noms suivantes :

-   Utilisez le même nom pour les propriétés **CN** et **lDAPDisplayName** d’un nouvel objet **attributeSchema** ou **classSchema** .
-   Identifiez la société avec un préfixe en minuscules dans la première section du nom. Ce préfixe peut être un nom DNS, un acronyme ou toute autre chaîne qui identifie de façon unique l’entreprise. Le préfixe garantit que tous les attributs et classes d’une société spécifique s’affichent consécutivement lors de la navigation dans le schéma.
-   Si vous développez une extension de schéma en tant que fournisseur de logiciels indépendant, ajoutez une abréviation du nom de produit du préfixe. Cela permet d’ajouter une distinction entre plusieurs produits qui contiennent des extensions de schéma LDAP.
-   Utilisez un trait d’Union comme caractère suivant après le préfixe.
-   Spécifiez un attribut ou un nom de classe qui est unique dans les attributs de la société après le trait d’Union. Cette partie du nom commun doit être descriptive. N’utilisez pas de noms illogique qui n’ont pas de sens pour les développeurs et les observateurs du schéma.

Par exemple, si la société fictive Fabrikam a étendu le schéma en ajoutant un attribut pour stocker un identificateur de courrier vocal, le nom **commun** et le **lDAPDisplayName** du nouvel attribut peuvent être « Fabrikam-VoiceMailID ».

Si le **lDAPDisplayName** d’un attribut ou d’une classe n’est pas spécifié, le système utilise le **CN** pour en générer un. Toutefois, l’algorithme système utilisé pour générer le nom peut entraîner des collisions de noms ou des noms difficiles à lire. Pour éviter ces problèmes, il est recommandé de spécifier explicitement **lDAPDisplayName** pour tous les attributs et les classes.

À des fins de développement et de test, il peut être souhaitable d’ajouter un suffixe de version au **CN** et à **lDAPDisplayName**, par exemple, « Fabrikam-VoiceMailID-001 ». Dans un environnement de développement/test distribué, un suffixe de version permet aux développeurs d’exécuter simultanément plusieurs versions de leurs logiciels. Une fois le test terminé, renommez l’attribut ou la classe pour supprimer le suffixe.

Il n’est pas possible de supprimer les versions obsolètes d’extensions de schéma, mais il est possible de les désactiver et de les renommer avec des noms obscurs. Pour plus d’informations, consultez [désactivation des classes et attributs existants](disabling-existing-classes-and-attributes.md).

 

 





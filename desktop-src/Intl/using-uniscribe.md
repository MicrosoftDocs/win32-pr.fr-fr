---
description: Uniscribe fournit des API pour prendre en charge la typographie et pour prendre en charge l’affichage et la modification de texte international, y compris les règles complexes de l’Asie du moyen et des scripts asiatiques.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Utilisation de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d5e4b6e02c2d6440281eafff54e43948edbe0a0259e969f3c564effb38092d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130039"
---
# <a name="using-uniscribe"></a>Utilisation de Uniscribe

Uniscribe fournit des API pour prendre en charge la typographie et pour prendre en charge l’affichage et la modification de texte international, y compris les règles complexes de l’Asie du moyen et des scripts asiatiques. Uniscribe fournit des routines de bas niveau pour gérer le texte entièrement mis en forme, et une API ScriptString simple définie pour le texte non mis en forme.

À l’aide de Uniscribe, les applications doivent uniquement gérer un magasin de stockage de codes de caractères Unicode. Les applications de disposition du texte n’ont pas besoin de gérer d’autres tampons ou tables de mappage pour suivre l’ordre des caractères. Chaque application ne doit stocker et gérer que l’ordre dans lequel les caractères sont entrés par l’utilisateur, ce qui correspond à l’ordre logique défini par Unicode. Le magasin de stockage ne change jamais suite à des opérations de disposition. Uniscribe gère un index à partir des clusters réorganisés jusqu’aux limites de caractères d’origine passées par l’application.

Les rubriques suivantes sont traitées dans cette section.

**Modélisation**

-   [Déterminer si un script nécessite la mise en forme de glyphes](determining-if-a-script-requires-glyph-shaping.md)
-   [Utilisation de moteurs de mise en forme](using-shaping-engines.md)

**Autre traitement**

-   [Mise en cache](caching.md)
-   [Affichage de texte avec Uniscribe](displaying-text-with-uniscribe.md)
-   [Traitement de scripts complexes](processing-complex-scripts.md)
-   [Utilisation de la police de secours](using-font-fallback.md)
-   [Utilisation des fonctions ScriptString](using-the-scriptstring-functions.md)

**Signe insertion**

-   [Affichage du signe insertion dans les chaînes bidirectionnelles](displaying-the-caret-in-bidirectional-strings.md)
-   [Gestion de l’emplacement du signe insertion et du test de positionnement](managing-caret-placement-and-hit-testing.md)
-   [Translation de l’offset X de l’accès à la souris à la position du signe insertion](translating-mouse-hit-x-offset-to-caret-position.md)

**Mots et clusters de caractères**

-   [Utilisation de clusters de caractères](using-character-clusters.md)
-   [Utilisation des points d’arrêt de mot](using-word-break-points.md)
-   [Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 




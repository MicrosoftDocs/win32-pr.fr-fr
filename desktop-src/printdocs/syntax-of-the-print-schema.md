---
description: En savoir plus sur la syntaxe du schéma d’impression, exprimée en syntaxe XML, et composée d’un petit nombre de types d’éléments.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntaxe du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405292"
---
# <a name="syntax-of-the-print-schema"></a>Syntaxe du schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma d’impression est exprimé en syntaxe XML. Les lecteurs sont donc censés être familiarisés avec la syntaxe XML et les termes tels que l’élément, la balise d’élément, le contenu de l’élément, l’attribut et l’espace de noms. L’infrastructure du schéma d’impression est composée d’un petit nombre de types d’éléments ; chaque type d’élément remplit un rôle spécifique dans les technologies basées sur le schéma d’impression.

Les types d’éléments se distinguent par leur balise d’élément XML. L’infrastructure du schéma d’impression définit la structure et l’organisation globales des technologies dépendantes, en indiquant pour chaque type d’élément quels types d’éléments sont autorisés en tant qu’éléments enfants.

De nombreux types d’éléments sont différenciés des autres du même type par l’attribut Name, qui joue un rôle significatif dans le schéma. L’attribut name sert à identifier les instances de chaque type d’élément. Les mots clés du schéma d’impression définissent un ensemble de valeurs pour l’attribut Name pour la plupart des types d’éléments. Dans la plupart des cas, les fournisseurs peuvent assigner leurs propres valeurs à l’attribut Name. Ils ont uniquement besoin de s’assurer que les valeurs sont XML QNames qualifié avec un espace de noms unique pour le fournisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




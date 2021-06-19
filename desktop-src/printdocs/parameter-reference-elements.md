---
description: En savoir plus sur les éléments ParameterRef dans l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Éléments ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396524"
---
# <a name="parameterref-elements"></a>Éléments ParameterRef

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les éléments ParameterRef s’appliquent spécifiquement aux éléments option, ce qui permet à cet élément d’option de faire référence à un élément ParameterDef particulier. Pour ces éléments d’option, un élément ScoredProperty qui caractérise l’option n’est pas codé en dur dans le document PrintCapabilities en tant que valeur, mais est plutôt variable. Pour activer cette variabilité, ces éléments ScoredProperty contiennent un élément ParameterRef. Un élément ScoredProperty ne peut pas contenir à la fois un élément Value et un élément ParameterRef. Les éléments option contenant un ou plusieurs éléments ParameterRef sont appelés éléments d’option paramétrables.

L’infrastructure du schéma d’impression permet à un élément d’option de contenir un nombre quelconque d’éléments ScoredProperty qui font référence à des éléments de paramètres, ainsi que n’importe quel nombre d’éléments ScoredProperty qui contiennent des éléments de valeur. L’infrastructure permet également à un nombre quelconque d’éléments de fonctionnalité de contenir des éléments d’option paramétrés, et un nombre quelconque d’éléments d’option paramétrables sont autorisés pour chaque élément de fonctionnalité. En outre, la même construction de paramètre peut être référencée par plusieurs éléments d’option différents, des éléments d’option qui peuvent appartenir à des éléments de fonctionnalité identiques ou différents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




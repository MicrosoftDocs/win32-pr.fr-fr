---
description: Windows La recherche utilise des ressources de langue, telles que des analyseurs lexicaux et des générateurs de formes dérivées, pour scinder le texte dans ses paramètres régionaux natifs lors de la création et du traitement des requêtes.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Extension des ressources linguistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed65c3539c477e256a0c40657ea4a99793feb9f6b33c95df416e3ad812fe39d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594709"
---
# <a name="extending-language-resources"></a>Extension des ressources linguistiques

Windows La recherche utilise des ressources de langue, telles que des analyseurs lexicaux et des générateurs de formes dérivées, pour scinder le texte dans ses paramètres régionaux natifs lors de la création et du traitement des requêtes. Microsoft fournit des analyseurs lexicaux et des générateurs de formes dérivées pour plusieurs langues. Cette section décrit comment implémenter et utiliser des analyseurs lexicaux et des générateurs de formes dérivées personnalisés pour des langues et des paramètres régionaux autres que ceux fournis par Microsoft.

-   [Fonctionnement des composants de ressources linguistiques](understanding-language-resource-components.md)
-   [Implémentation d’un analyseur lexical et du générateur de formes dérivées](implementing-a-word-breaker-and-stemmer.md)
-   [Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md)
-   [Ressources et meilleures pratiques pour la résolution des problèmes](troubleshooting-language-resources.md)

## <a name="additional-resources"></a>Ressources supplémentaires

-   pour obtenir la liste des lanuages prises en charge par les analyseurs lexicaux, consultez [langues prises en charge par Windows Search](-search-3x-wds-language-support.md).
-   si vous devez identifier la langue d’un morceau de texte, vous pouvez utiliser la détection automatique de la langue (diagnostic linux), disponible dans Windows 7 et versions ultérieures. Pour plus d’informations, consultez [services linguistiques étendus](../intl/extended-linguistic-services.md) (ELS).
-   Pour obtenir la documentation de référence applicable, consultez [interfaces de complément de données](-search-data-addins-interfaces-entry-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Extension de l’index](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 

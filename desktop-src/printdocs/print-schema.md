---
description: Cette vue d’ensemble décrit le schéma d’impression et les liens vers les rubriques de référence du schéma d’impression. Le schéma d’impression comprend les mots clés du schéma d’impression et le Framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Référence du schéma d’impression hérité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540496004534dff3e66ce1c30415ccec14c6d7b31c59ecf2f79905c25d5e7861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470856"
---
# <a name="legacy-print-schema-reference"></a>Référence du schéma d’impression hérité

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

le schéma d’impression et les technologies associées sont disponibles dans microsoft .NET Framework 3,0, microsoft Windows Vista et versions ultérieures.

Le schéma d’impression fournit un format XML pour l’expression et l’organisation d’un grand ensemble de propriétés qui décrivent un format de travail ou PrintCapabilities de manière hiérarchique.

Le schéma d’impression est un terme générique qui comprend deux composants : les mots clés du schéma d’impression et l’infrastructure du schéma d’impression. Le document des mots clés du schéma d’impression est un schéma public qui définit un ensemble d’instances d’éléments qui peuvent être utilisées pour décrire les attributs des appareils et la mise en forme du travail d’impression. L’infrastructure du schéma d’impression est un schéma public qui définit une collection hiérarchique de types d’éléments XML et spécifie la manière dont les types d’éléments peuvent être utilisés ensemble.

Les mots clés du schéma d’impression et l’infrastructure du schéma d’impression constituent la base de deux technologies liées au schéma d’impression, du schéma PrintCapabilities et du schéma PrintTicket.

Il est important de garder à l’esprit que l’un des objectifs du schéma d’impression est de prendre en charge les extensions de schéma par les fournisseurs. Autrement dit, les fournisseurs ne sont pas limités à l’utilisation uniquement des instances de propriété, de fonctionnalité, d’option ou de ParameterInit définies dans les mots clés du schéma d’impression dans les technologies basées sur l’infrastructure du schéma d’impression. Les instances d’éléments spécifiques au fournisseur peuvent être disséminées librement dans des instances d’élément définies dans les mots clés du schéma d’impression. La seule exigence est que les instances de propriétés spécifiques au fournisseur (c’est-à-dire, privées) doivent appartenir à un espace de noms qui est clairement associé au fournisseur.

-   [Arrière-plan du schéma d’impression](print-schema-background.md)

-   [Imprimer des technologies Schema-Related](print-schema-related-technologies.md)

-   [Termes utilisés dans le schéma d’impression](terms-used-in-the-print-schema.md)

-   [Syntaxe du schéma d’impression](syntax-of-the-print-schema.md)

-   [Résumé des types d’éléments](summary-of-element-types.md)

-   [Structure du schéma d’impression](print-schema-framework.md)

-   [Mots clés publics du schéma d’impression](print-schema-public-keywords.md)

-   [Schéma PrintCapabilities et construction de document](printcapabilities-schema-and-document-construction.md)

-   [Schéma PrintTicket et construction de document](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




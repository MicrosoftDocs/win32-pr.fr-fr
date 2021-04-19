---
description: L’API de document XPS implémente le modèle d’objet XPS et permet aux développeurs de créer un modèle d’objet XPS, de manipuler le contenu d’un document XPS dans des programmes Windows natifs \\ \\ et d’enregistrer le modèle d’objet XPS dans un fichier ou un flux de données en tant que document XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: À propos de l’API de document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536564"
---
# <a name="about-xps-document-api"></a>À propos de l’API de document XPS

L' [API de document XPS](documents-xps.md) implémente le modèle d’objet XPS et permet aux développeurs de créer un modèle d’objet XPS, de manipuler le contenu d’un document XPS dans des programmes Windows natifs \\ \\ et d’enregistrer le modèle d’objet XPS dans un fichier ou un flux de données en tant que document XPS. Les développeurs de modules de pipeline de filtre XPSDrv peuvent également utiliser l’API de document XPS pour manipuler le contenu d’un document XPS dans un filtre de pilote d’imprimante XPSDrv.

## <a name="xps-document-api-overview"></a>Vue d’ensemble de l’API de document XPS

Le modèle objet XPS est le modèle d’informations d’un document XPS. Le modèle d’information du document XPS est distinct du modèle de balisage utilisé à l’intérieur des parties du document. Le modèle d’objet XPS décrit l’Organisation des composants internes qui composent un document XPS, et le modèle de balisage décrit le contenu de ces composants.

Dans un programme, le modèle objet XPS est instancié comme un modèle d’objet XPS. Le modèle d’objet XPS est essentiellement une version en mémoire du contenu d’un document XPS. Bien qu’il soit similaire dans une organisation logique à un document XPS, un modèle d’objet XPS n’est pas considéré comme un document XPS tant qu’il n’a pas été sérialisé dans un fichier ou un flux.

La structure exacte du balisage n’est pas disponible pour le modèle d’objet XPS lorsqu’un document XPS est désérialisé du balisage à un modèle d’objet XPS. Par exemple, si la propriété a été représentée comme un élément ou un attribut dans le balisage, la valeur de la propriété d’un objet document est présentée par le modèle OM XPS exactement de la même façon.

L' [API de document XPS](documents-xps.md) peut être divisée selon les catégories suivantes :

-   [Interfaces du Trunk XPS OM](xps-om-trunk-interfaces.md)

    Les interfaces Trunk fournissent l’accès aux composants de niveau supérieur de la structure de document XPS. Ces interfaces fournissent également les moyens de sérialiser un modèle d’objet XPS et de désérialiser un document XPS.

-   [Interfaces de page OM XPS](xps-object-model-page-interfaces.md)

    Les interfaces de page donnent accès au contenu d’une page dans un document XPS. Les interfaces qui décrivent le contenu de la page sont également incluses avec les interfaces de page.

-   [Signatures numériques XPS OM](using-the-xps-digital-signatures.md)

    Le modèle d’objet XPS prend en charge les signatures numériques. Toutefois, vous pouvez accéder aux signatures numériques dans un document XPS directement sans créer un modèle d’objet XPS. Pour plus d’informations sur l’accès aux signatures numériques XPS sans modèle XPS, consultez [API de signature numérique XPS](xps-digital-signatures.md).

-   [Interfaces du ticket d’impression XPS OM](xps-object-model-print-ticket-interfaces.md)

    Les documents XPS prennent en charge les tickets d’impression au niveau du package (travail), du document et de la page. Les tickets d’impression contiennent des informations sur la mise en forme du contenu du document pour l’impression ou l’affichage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Dans cette section**
</dt> <dt>

[Interfaces du Trunk XPS OM](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfaces de page OM XPS](xps-object-model-page-interfaces.md)
</dt> <dt>

[Signatures numériques XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfaces du ticket d’impression XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Autres rubriques connexes**
</dt> <dt>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)
</dt> <dt>

[Signatures numériques XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




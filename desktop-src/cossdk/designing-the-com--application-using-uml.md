---
description: Le développement d’une application COM+ réussie nécessite une conception architecturale d’application initiale.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Conception de l’application COM+ à l’aide d’UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b5ab7cc96d753e023f8b89825ce7540c5abc6d79b7b78f231eea8cce4e2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916733"
---
# <a name="designing-the-com-application-using-uml"></a>Conception de l’application COM+ à l’aide d’UML

Le développement d’une application COM+ réussie nécessite une conception architecturale d’application initiale. Le langage UML (UML) est essentiel à ce développement de conception. Le UML est une notation de modélisation pour les données d’application et les processus qui combine les meilleures pratiques de l’industrie des logiciels. Étant donné que le langage UML divise l’application en trois vues reflétant l’application, ainsi que son Packaging et sa mise en œuvre, la notation de modélisation s’étend bien à la prise en charge de la modélisation d’entreprise.

Le UML traite trois vues de l’application, comme suit :

-   Vue statique, modélisée par les informations tirées des scénarios utilisateur et des diagrammes de classes.
-   Vue dynamique, modélisée à l’aide de diagrammes de séquence, de collaboration et de transition d’État.
-   La vue fonctionnelle, qui est le texte descriptif le plus traditionnel qui utilise le pseudocode et les spécifications.

Les informations de ces vues peuvent être collectées en suivant trois étapes de conception qui fonctionnent bien avec le langage UML. Avant d’écrire une seule ligne de code, vous devez créer les modèles suivants :

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modèle conceptuel
</dt> <dd>

Déterminez les composants et services requis.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modèle logique
</dt> <dd>

Déterminez le niveau de conception logique auquel ils appartiennent.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modèle physique
</dt> <dd>

Déterminez où les composants résident physiquement et comment ils doivent être codés.

</dd> </dl>

Ces modèles peuvent ensuite être utilisés avec des outils de cas UML. Pour plus d’informations sur ces trois modèles de conception, consultez les rubriques suivantes dans cette section :

-   [Modèle conceptuel : exigences de l’application](the-conceptual-model--application-requirements.md)
-   [Modèle logique : définition et planification de l’application](the-logical-model--application-definition-and-planning.md)
-   [Modèle physique : architecture de l’application](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hypothèses et principes de conception de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Astuces de conception générale pour l’utilisation de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimisation des interactions avec le niveau de logique métier COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Autres outils Microsoft pour la création d’applications distribuées](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




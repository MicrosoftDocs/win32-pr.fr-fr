---
description: Cette rubrique décrit comment la source Sequencer gère les durées de présentation pendant la lecture.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Durée des présentations de séquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45ea9c8b315171365810f33bb9a66ca4d223fb2119d7aea19288c3ebdd93ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238365"
---
# <a name="sequence-presentation-times"></a>Durée des présentations de séquence

Cette rubrique décrit comment la [source Sequencer](sequencer-source.md) gère les durées de présentation pendant la lecture.

## <a name="overview"></a>Vue d’ensemble

La source Sequencer prend en charge deux modes différents : les séquences de sélection et les séquences de modification.

Dans une séquence d’édition, l’application spécifie la durée de chaque segment à l’avance, avant de commencer la lecture. Dans une séquence de sélection, l’application ne spécifie pas la durée à l’avance. (En fait, la durée n’est peut-être pas connue.)

Dans les deux cas, vous pouvez spécifier le début et l’heure d’arrêt du support d’un segment. Ces heures spécifient la position dans le fichier source où le segment commence et se termine. Par exemple, supposons que le fichier source soit de 90 secondes. Si vous souhaitez supprimer les 10 premières secondes et les 10 dernières secondes, vous devez spécifier les valeurs suivantes :

-   Début du média : 10 secondes
-   Arrêt du support : 80 secondes

Pour spécifier l’heure de début du support, définissez l’attribut [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) sur le nœud source. Pour spécifier l’heure d’arrêt du support, définissez l’attribut [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) sur le nœud source.

Pour créer une séquence d’édition, définissez l’attribut [ \_ \_ \_ heure globale de session MF](mf-session-global-time-attribute.md) lorsque vous créez la session multimédia. Dans le cas contraire, la session multimédia attend des séquences de sélection. Dans une séquence d’édition, chaque topologie de segment doit avoir l’attribut [ \_ \_ PROJECTSTART de topologie MF](mf-topology-projectstart-attribute.md) et l’attribut [ \_ \_ PROJECTSTOP de topologie MF](mf-topology-projectstop-attribute.md) .

## <a name="playlist-sequences"></a>Séquences de sélection

Dans une séquence de sélection, l’horloge de la présentation démarre à zéro et continue à travers les limites du segment. Les sources natives fournissent des exemples avec des horodatages égaux à l’heure du support. Le pipeline convertit les horodatages à l’heure de présentation correcte comme suit :

-   Nouvel horodatage = durée du média + décalage − début du média

La valeur de *offset* est l’heure de présentation à laquelle le segment précédent s’est terminé. Pour le premier segment, le décalage est égal à zéro. Voici deux exemples montrant comment ces conversions de datage sont calculées :

-   Exemple 1 : Supposons que le premier segment (S1) soit de 10 secondes et que le second segment (S2) ait une heure de début de support de zéro. La source Native utilise l’heure du support pour ses horodatages, donc le premier échantillon de S2 a un horodatage égal à zéro. Le décalage est de 10 secondes (la durée S1). l’horodatage ajusté est donc : 0 + 10 − 0 = 10 secondes.
-   Exemple 2 : Supposons que le segment S1 ait une longueur de 10 secondes, tandis que S2 a une heure de début de support de 5 secondes. Le premier échantillon de S2 a un horodatage de 5 secondes (heure du support). Le décalage est de 10 secondes. l’horodatage ajusté est donc : 5 + 10 − 5 = 10 secondes.

Tous les composants de pipeline en aval des nœuds sources reçoivent des exemples avec les horodatages ajustés. Les nœuds sources d’une topologie peuvent avoir des heures de début de support différentes. les ajustements sont donc calculés séparément pour chaque branche de la topologie.

Lorsque la présentation passe au segment suivant, l’horloge de la présentation ne s’arrête pas ou n’est pas réinitialisée, et l’heure de la présentation augmente de façon monotone. Avant le début d’un nouveau segment, la session multimédia envoie un événement [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) à l’application. L’événement spécifie l’heure de début du segment, par rapport à l’horloge de présentation, et la valeur de l’offset. Lorsqu’un nouveau segment démarre, le pipeline appelle [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) sur la source de Sequencer avec la valeur VT \_ vide. La source Sequencer envoie un événement [MESourceStarted](mesourcestarted.md) sans heure de début.

Pour rechercher, l’application spécifie un identificateur de segment plus un décalage horaire dans le segment. Après la recherche, l’horloge de la présentation commence à l’offset du *segment* . Voici un exemple de fonctionnement de ce processus :

-   Exemple 3 : l’application cherche à segmenter S3, avec un décalage de segment de 10 secondes. L’horloge de présentation démarre à 10 secondes (décalage de segment). Le décalage n’inclut pas la durée des segments S1 et S2. La source Sequencer envoie un événement [MESourceStarted](mesourcestarted.md) avec une heure de début égale au décalage de segment, 10 secondes.

Après une recherche, si la lecture continue jusqu’au segment suivant, la transition fonctionne comme les exemples précédents, à ceci près que le décalage n’inclut pas les segments ignorés.

Voici des informations supplémentaires qui affectent la façon dont les exemples sont horodatés :

-   Les décodeurs peuvent nécessiter des données au-delà du temps d’arrêt du support. Le pipeline extrait le plus de données de la source que le décodeur requiert, puis supprime les exemples de sortie du décodeur.
-   Les transformations peuvent mettre des données en mémoire tampon. Par exemple, un effet audio peut être nécessaire. Lorsqu’un segment se termine, l’horodatage du dernier échantillon de la transformation est antérieur à la fin du segment, car la transformation contient des données. Au démarrage du segment suivant, l’horodatage sur le premier échantillon est légèrement antérieur au début du segment. Il n’y a pas d’écart dans les horodatages, donc les données qui atteignent le récepteur multimédia sont continues. Lorsque le segment final se termine, le pipeline draine la transformation, de sorte qu’aucune donnée n’est perdue.
-   La source doit peut-être démarrer légèrement avant l’heure de début du support, pour sélectionner l’image clé précédente. Par conséquent, après l’ajustement, le premier exemple peut avoir une heure de présentation négative.

## <a name="editing-sequences"></a>Modification des séquences

Dans une séquence d’édition, l’application spécifie les limites de segment à l’avance, en définissant les attributs de [**\_ topologie MF \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) et de [**\_ topologie MF \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . Le pipeline calcule les ajustements pour les horodatages de la même façon que pour une séquence de sélection :

-   Pour le décalage, elle utilise la valeur de [**la \_ topologie MF \_ PROJECTSTART**](mf-topology-projectstart-attribute.md), au lieu d’utiliser la fin observée du segment.

-   Pour la recherche, le décalage utilise une valeur égale à la valeur [**\_ \_ PROJECTSTART de la topologie MF**](mf-topology-projectstart-attribute.md) du segment plus le décalage de segment.

Par conséquent, l’heure de présentation dans une séquence de modification est toujours relative au début de la présentation, même si l’application recherche un autre segment.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 




---
description: Cette rubrique décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez Media Foundation Guide de programmation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Vue d’ensemble de l’architecture Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104565336"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Vue d’ensemble de l’architecture Media Foundation

Cette rubrique décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez [Media Foundation Guide de programmation](media-foundation-programming-guide.md).

Le diagramme suivant présente une vue d’ensemble de l’architecture Media Foundation.

![Diagramme montrant une vue d’ensemble de l’architecture de Media Foundation.](images/mfarch01.png)

Media Foundation fournit deux modèles de programmation distincts. Le premier modèle, affiché sur le côté gauche du diagramme, utilise un pipeline de bout en bout pour les données multimédias. L’application initialise le pipeline, par exemple en fournissant l’URL d’un fichier à lire, puis appelle les méthodes pour contrôler la diffusion en continu. Dans le deuxième modèle, indiqué sur le côté droit du diagramme, l’application extrait les données d’une source ou les transmet à une destination (ou les deux). Ce modèle est particulièrement utile si vous avez besoin de traiter les données, car l’application a un accès direct au flux de données.

### <a name="primitives-and-platform"></a>Primitives et plateforme

À partir du bas du diagramme, les *primitives* sont des objets d’assistance utilisés dans l’API Media Foundation :

-   Les [attributs](attributes-and-properties.md) sont un moyen générique de stocker des informations à l’intérieur d’un objet, sous la forme d’une liste de paires clé/valeur.
-   Les [types de médias](media-types.md) décrivent le format d’un flux de données multimédia.
-   Les [mémoires tampons de média](media-buffers.md) contiennent des blocs de données multimédias, tels que des images vidéo et des échantillons audio, et sont utilisés pour transporter des données entre des objets.
-   Les [exemples de supports](media-samples.md) sont des conteneurs pour les mémoires tampons de média. Elles contiennent également des métadonnées sur les mémoires tampons, telles que les horodatages.

Les [API de plateforme Media Foundation](media-foundation-platform-apis.md) fournissent certaines fonctionnalités de base utilisées par le pipeline Media Foundation, telles que les rappels asynchrones et les files d’attente de travail. Certaines applications peuvent avoir besoin d’appeler ces API directement. en outre, vous en aurez besoin si vous implémentez une source, une transformation ou un récepteur personnalisé pour Media Foundation.

### <a name="media-pipeline"></a>Pipeline de média

Le pipeline de média contient trois types d’objets qui génèrent ou traitent des données multimédias :

-   Les [sources multimédias](media-sources.md) introduisent des données dans le pipeline. Une source de média peut obtenir des données à partir d’un fichier local, tel qu’un fichier vidéo ; à partir d’un flux réseau ; ou à partir d’un périphérique de capture matérielle.
-   [Media Foundation transforme](media-foundation-transforms.md) les données de processus (MFTS) à partir d’un flux. Les encodeurs et les décodeurs sont implémentés en tant que MFTs.
-   Les [récepteurs de médias](media-sinks.md) consomment les données ; par exemple, en affichant une vidéo sur l’écran, en lisant l’audio ou en écrivant les données dans un fichier multimédia.

Des tiers peuvent implémenter leurs propres sources personnalisées, récepteurs et MFTs. par exemple, pour prendre en charge de nouveaux formats de fichiers multimédias.

La [session multimédia](media-session.md) contrôle le flux de données via le pipeline et gère les tâches telles que le contrôle de qualité, la synchronisation audio/vidéo et la réponse aux modifications de format.

### <a name="source-reader-and-sink-writer"></a>Lecteur source et enregistreur du récepteur

Le [lecteur source](source-reader.md) et le [writer du récepteur](sink-writer.md) offrent un autre moyen d’utiliser les composants de base du Media Foundation (sources de média, transformations et récepteurs multimédias). Le lecteur source héberge une source multimédia et zéro ou plusieurs décodeurs, tandis que le writer du récepteur héberge un récepteur multimédia et zéro ou plusieurs encodeurs. Vous pouvez utiliser le lecteur source pour obtenir des données compressées ou non compressées à partir d’une source multimédia, et utiliser le writer de récepteur pour encoder les données et les envoyer à un récepteur multimédia.

> [!Note]  
> Le lecteur source et le writer du récepteur sont disponibles dans Windows 7.

 

Ce modèle de programmation offre à l’application davantage de contrôle sur le workflow des données et donne également à l’application un accès direct aux données à partir de la source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Media Foundation : notions essentielles](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




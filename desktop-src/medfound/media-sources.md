---
description: Sources multimédias
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Sources multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211228"
---
# <a name="media-sources"></a>Sources multimédias

Les *sources multimédias* sont des objets qui génèrent des données multimédias dans le pipeline Media Foundation. Cette section décrit en détail les API source des médias. Lisez cette section si vous implémentez une source de média personnalisée, ou si vous utilisez une source de média en dehors du pipeline Media Foundation.

Si votre application utilise la couche de contrôle, elle n’a besoin d’utiliser qu’un sous-ensemble limité des API sources du média. Pour plus d’informations, consultez la rubrique [utilisation de sources multimédias avec la session multimédia](using-media-sources-with-the-media-session.md).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Modèle d’objet de source multimédia](media-source-object-model.md)<br/>                                 | Cette rubrique décrit le modèle d’objet pour les sources multimédias dans Microsoft Media Foundation<br/>                     |
| [Descripteurs de présentation](presentation-descriptors.md)<br/>                                   | Un *descripteur de présentation* est un objet qui contient la description d’une présentation particulière.<br/>      |
| [Événements de source de média](media-source-events.md)<br/>                                             | Cette rubrique répertorie les événements qui sont envoyés par les sources de média et les flux multimédias.<br/>                             |
| [Écriture d’une source de média personnalisée](writing-a-custom-media-source.md)<br/>                         | Cette rubrique décrit comment implémenter une source de média personnalisée dans Media Foundation.<br/>                          |
| [Étude de cas : source de média MPEG-1](tutorial--writing-a-custom-media-source.md)<br/>             | Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) [source de média MPEG-1](mpeg1source-sample.md) .<br/>        |
| [Fournisseurs de métadonnées personnalisés pour les fichiers multimédias](custom-metadata-providers-for-media-files.md)<br/> | Cette rubrique explique comment écrire un gestionnaire de propriétés de shell personnalisé pour une source de média Media Foundation.<br/>    |
| [Résolveur source](source-resolver.md)<br/>                                                     | Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Fournisseurs de métadonnées personnalisés pour les fichiers multimédias](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 





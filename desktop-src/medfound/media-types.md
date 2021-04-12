---
description: Types de médias
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Types de médias (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321625"
---
# <a name="media-types-media-foundation"></a>Types de médias (Media Foundation)

Un *type de média* est un moyen de décrire le format d’un flux multimédia. Dans Media Foundation, les types de média sont représentés par l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Les applications utilisent des types de médias pour découvrir le format d’un fichier multimédia ou d’un flux de média. Les objets du pipeline Media Foundation utilisent des types de média pour négocier les formats qu’ils distribueront ou recevront.

Cette section contient les rubriques suivantes :



| Rubrique                                                                    | Description                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [À propos des types de média](about-media-types.md)                               | Vue d’ensemble générale des types de médias dans Media Foundation.                             |
| [GUID de type de média](media-type-guids.md)                                 | Répertorie les GUID définis pour les principaux types et sous-types.                            |
| [Types de média audio](audio-media-types.md)                               | Comment créer des types de média pour les formats audio.                                     |
| [Types de média vidéo](video-media-types.md)                               | Comment créer des types de média pour les formats vidéo.                                     |
| [Types de média complets et partiels](complete-and-partial-media-types.md) | Décrit la différence entre les types de média complets et les types de média partiels.   |
| [Conversions de type de média](media-type-conversions.md)                     | Comment effectuer une conversion entre des types de média Media Foundation et des structures de format plus anciennes. |
| [Fonctions d’assistance du type de média](media-type-helper-functions.md)           | Liste des fonctions qui manipulent ou obtiennent des informations à partir d’un type de média.        |
| [Code de débogage du type de média](media-type-debugging-code.md)               | Exemple de code qui montre comment afficher un type de média lors du débogage.                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives de Media Foundation](media-foundation-primitives.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




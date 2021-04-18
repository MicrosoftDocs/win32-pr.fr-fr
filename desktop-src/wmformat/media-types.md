---
title: Types de médias pour Windows Media Format SDK
description: En savoir plus sur les types de médias qui peuvent être utilisés par le kit de développement logiciel (SDK) Windows Media format. Les types de média sont des valeurs GUID affectées à des constantes dans le kit de développement logiciel (SDK).
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, types de média
- ASF (Advanced Systems Format), types de média
- ASF (format des systèmes avancés), types de média
- types de média, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106533528"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Types de médias pour Windows Media Format SDK

Les types de médias identifient les différents types de médias qui peuvent être utilisés par le kit de développement logiciel (SDK) Windows Media format. Tous les types de média sont des valeurs GUID qui ont été affectées à des constantes dans le kit de développement logiciel (SDK). Les valeurs GUID représentées par les constantes répertoriées dans cette section sont répertoriées dans la section [identificateurs de type de média](media-type-identifiers.md) de cette référence.

Le tableau suivant répertorie les principaux types de médias. Ces constantes définissent la classification générale des supports numériques pris en charge par le kit de développement logiciel (SDK) du format Windows Media.



| Type principal                | Description                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| \_Vidéo WMMEDIATYPE        | Flux vidéo.                                                                                         |
| WMMEDIATYPE \_ audio        | Flux audio.                                                                                        |
| \_Script WMMEDIATYPE       | Flux de script.                                                                                        |
| WMMEDIATYPE \_ filetransfer | Flux qui contient des fichiers de données. Les flux Web, qui se composent de fichiers HTML, ont également ce type majeur. |
| \_Image WMMEDIATYPE        | Flux d’images JPEG pour un fichier audio illustré (comme dans un diaporama).                                 |
| \_Texte WMMEDIATYPE         | Flux de texte.                                                                                          |



 

Outre les types de média majeurs pris en charge explicitement, vous pouvez créer vos propres types de données arbitraires. Pour les types de données arbitraires personnalisés, vous devez vous assurer que le GUID que vous utilisez ne correspond pas à un type majeur existant.

Un flux de média aura souvent un sous-type en plus de son type principal. Les sections suivantes répertorient les sous-types pris en charge.



| Section                                                        | Description                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Sous-types de médias non compressés](uncompressed-media-subtypes.md) | Décrit les sous-types disponibles pour les médias non compressés. Ce sont les types généralement associés à un média d’entrée ou de sortie.              |
| [Sous-types de média compressés](compressed-media-subtypes.md)     | Décrit les sous-types disponibles pour les médias compressés. Ce sont les types généralement associés à des médias dans un flux d’un fichier ASF. |
| [Formats d’entrée vidéo](video-input-formats.md)                 | Répertorie les formats vidéo acceptés en tant qu’entrées pour le codec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs de type de média**](media-type-identifiers.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 





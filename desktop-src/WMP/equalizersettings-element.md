---
title: Élément EQUALIZERSETTINGS
description: Élément EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- habillages Lecteur Windows Media, élément EQUALIZERSETTINGS
- habillages, élément EQUALIZERSETTINGS
- Élément EQUALIZERSETTINGS
- informations de référence sur les habillages, élément EQUALIZERSETTINGS
- éléments, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: facd5d9630536947614166bc8444ad38e33020920ce679180824ef9a3b007bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650949"
---
# <a name="equalizersettings-element"></a>Élément EQUALIZERSETTINGS

l’élément **EQUALIZERSETTINGS** fournit un moyen de manipuler l’égaliseur graphique et d’autres paramètres audio de Lecteur Windows Media à l’aide des attributs et de la méthode répertoriés ici.

L’élément **EQUALIZERSETTINGS** prend en charge les attributs suivants.



| Attribut                                                          | Description                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [bandes](equalizersettings-bands.md)                               | Récupère le nombre de bandes de fréquence prises en charge.                                                      |
| [omettre](equalizersettings-bypass.md)                             | Spécifie ou récupère une valeur indiquant si le filtre d’égaliseur est contourné dans le graphique de filtre. |
| [Fondu enchaîné](equalizersettings-crossfade.md)                       | Spécifie ou récupère une valeur indiquant si le fondu croisé est activé.                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | Spécifie ou récupère la quantité de chevauchement de fondu croisé en millisecondes.                                |
| [currentPreset](equalizersettings-currentpreset.md)               | Spécifie ou récupère l’index de la présélection actuelle.                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | Récupère le titre de la présélection actuelle.                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | Récupère le nom du paramètre de haut-parleur actuel.                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | Spécifie ou récupère une valeur indiquant si la tension de la spline est activée ou désactivée.                |
| [enhancedAudio](equalizersettings-enhancedaudio.md)               | Spécifie ou récupère une valeur indiquant si l’audio étendu est activé.                          |
| [gainLevels](equalizersettings-gainlevels.md)                     | Spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.                  |
| [gainLevel1](equalizersettings-gainlevel1.md)                     | Spécifie ou récupère le niveau de gain de la bande 1.                                                        |
| [gainLevel2](equalizersettings-gainlevel2.md)                     | Spécifie ou récupère le niveau de gain de la bande 2.                                                        |
| [gainLevel3](equalizersettings-gainlevel3.md)                     | Spécifie ou récupère le niveau de gain de la bande 3.                                                        |
| [gainLevel4](equalizersettings-gainlevel4.md)                     | Spécifie ou récupère le niveau de gain de la bande 4.                                                        |
| [gainLevel5](equalizersettings-gainlevel5.md)                     | Spécifie ou récupère le niveau de gain de la bande 5.                                                        |
| [gainLevel6](equalizersettings-gainlevel6.md)                     | Spécifie ou récupère le niveau de gain de la bande 6.                                                        |
| [gainLevel7](equalizersettings-gainlevel7.md)                     | Spécifie ou récupère le niveau de gain de la bande 7.                                                        |
| [gainLevel8](equalizersettings-gainlevel8.md)                     | Spécifie ou récupère le niveau de gain de la bande 8.                                                        |
| [gainLevel9](equalizersettings-gainlevel9.md)                     | Spécifie ou récupère le niveau de gain de la bande 9.                                                        |
| [gainLevel10](equalizersettings-gainlevel10.md)                   | Spécifie ou récupère le niveau de gain de la bande 10.                                                       |
| [normalisation](equalizersettings-normalization.md)               | Spécifie ou récupère une valeur indiquant si la normalisation est activée.                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | Récupère la valeur de normalisation moyenne.                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | Récupère la valeur de normalisation de pointe.                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | Récupère le nombre de présélections disponibles.                                                              |
| [Haut-parleur](equalizersettings-speakersize.md)                   | Spécifie ou récupère l’index de la taille actuelle de l’orateur.                                           |
| [splineTension](equalizersettings-splinetension.md)               | Spécifie ou récupère la tension de la spline pour le contrôle égaliseur.                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | Spécifie ou récupère le niveau de TruBass du SRS.                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | Spécifie ou récupère le niveau de l’effet SRS WOW.                                                        |



 

L’élément **EQUALIZERSETTINGS** prend en charge les méthodes suivantes.



| Méthode                                                 | Description                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | Applique la présélection d’égaliseur suivante.                                   |
| [presetTitle](equalizersettings-presettitle.md)       | Récupère le nom de la présélection de l’égaliseur avec l’index spécifié. |
| [previousPreset](equalizersettings-previouspreset.md) | Applique la présélection précédente de l’égaliseur.                               |
| [reset](equalizersettings-reset.md)                   | Rétablit les niveaux de gain de toutes les bandes à zéro décibels.                |



 

L’élément **EQUALIZERSETTINGS** peut implémenter les gestionnaires d’événements [ \_ OnChange d’attribut](attribute-onchange.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 





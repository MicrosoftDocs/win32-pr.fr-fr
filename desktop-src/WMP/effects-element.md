---
title: Élément EFFECTs
description: Élément EFFECTs
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- apparences de Lecteur Windows Media, élément effects
- Skins, élément EFFECTs
- Élément EFFECTs
- informations de référence sur les apparences, élément EFFECTs
- éléments, effets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651139"
---
# <a name="effects-element"></a>Élément EFFECTs

L’élément **Effects** permet d’organiser et de manipuler des visualisations à l’aide des méthodes et attributs suivants. Un élément d' **effets** prédéfinis est également fourni pour des raisons pratiques.

L’élément **Effects** prend en charge les attributs suivants.



| Attribut                                                        | Description                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AutoriserTout](effects-allowall.md)                                 | Spécifie ou récupère une valeur indiquant s’il faut inclure toutes les visualisations dans le registre.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Spécifie ou récupère la visualisation actuelle.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Récupère le nombre de présélections disponibles pour la visualisation actuelle.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Récupère le titre d’affichage de la visualisation actuelle.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Récupère le nom du registre de la visualisation actuelle.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Spécifie ou récupère la présélection actuelle de la visualisation actuelle.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Récupère le titre de la présélection actuelle de la visualisation actuelle.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Récupère une valeur indiquant si la visualisation en cours peut être affichée en mode plein écran.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Récupère le nombre de visualisations disponibles.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Récupère une valeur indiquant si la visualisation en cours a une page de propriétés.                                                                                                                                                                  |
| [Large](effects-fullscreen.md)                             | Spécifie ou récupère une valeur indiquant si la visualisation en cours est affichée en mode plein écran. Ne peut être défini qu’au moment de l’exécution.                                                                                                                   |
| [fenêtrées](effects-windowed.md)                                 | Spécifie ou récupère une valeur indiquant si la visualisation sera affichée en fenêtre ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment ou s’il peut être coupé. Ne peut être défini qu’au moment de la conception. |



 

L’élément **Effects** prend en charge les méthodes suivantes.



| Méthode                                       | Description                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Récupère le nom convivial de la visualisation avec l’index de Registre spécifié.                               |
| [effectType](effects-effecttype.md)         | Récupère le nom du registre de la visualisation avec l’index de Registre spécifié.                               |
| [suivant](effects-next.md)                     | Affiche la présélection de visualisation suivante, en passant à la visualisation suivante, si nécessaire.                            |
| [nextEffect](effects-nexteffect.md)         | Affiche la première présélection de la visualisation suivante, en ignorant les présélections intermédiaires.                                |
| [nextPreset](effects-nextpreset.md)         | Affiche la présélection suivante de la visualisation actuelle.                                                            |
| [previous](effects-previous.md)             | Affiche la présélection de visualisation précédente, en passant à la dernière présélection de la visualisation précédente, si nécessaire. |
| [previousEffect](effects-previouseffect.md) | Affiche la visualisation précédente, en ignorant les présélections.                                                            |
| [previousPreset](effects-previouspreset.md) | Affiche la présélection précédente de la visualisation actuelle.                                                        |
| [settings](effects-settings.md)             | Affiche la page d’attributs pour la visualisation actuelle, le cas échéant.                                            |



 

L’élément **Effects** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).

Les effets prédéfinis sont des éléments d' **effet** normal avec différents paramètres d’attribut communs spécifiés par défaut. Les effets prédéfinis suivants sont disponibles.



| EFFETS prédéfinis           | Description                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Élément **Effects** qui itère au sein des effets disponibles. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 





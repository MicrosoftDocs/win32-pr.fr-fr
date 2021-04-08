---
title: Controls (objet)
description: L’objet Controls permet de manipuler la lecture des médias à l’aide des propriétés et méthodes suivantes.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Contrôle l’objet Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678833"
---
# <a name="controls-object"></a>Controls (objet)

L’objet **Controls** permet de manipuler la lecture des médias à l’aide des propriétés et méthodes suivantes.

L’objet **Controls** prend en charge les propriétés suivantes.



| Propriété                                                            | Description                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | Récupère le nombre de langues audio prises en charge.                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | Spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | Spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.                                                   |
| [currentItem](controls-currentitem.md)                             | Spécifie ou récupère l’élément multimédia actuel.                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | Spécifie ou récupère le numéro de marqueur actuel.                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | Spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | Récupère la position actuelle dans l’élément multimédia sous la forme d’une **chaîne**.                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Spécifie ou récupère la position actuelle dans l’élément multimédia en cours à l’aide d’un format de code temporel. Cette propriété prend actuellement en charge le code de temps SMPTE. |
| [isAvailable](controls-isavailable.md)                             | Récupère une valeur indiquant si un type d’informations spécifié est disponible ou si une action donnée peut être exécutée.                                                |



 

L’objet **Controls** prend en charge les méthodes suivantes.



| Méthode                                                                  | Description                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [fastForward](controls-fastforward.md)                                 | Démarre la lecture rapide de l’élément multimédia dans le sens avant.                                     |
| [fastReverse](controls-fastreverse.md)                                 | Démarre la lecture rapide de l’élément multimédia dans le sens inverse.                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | Récupère la description de la langue audio correspondant à l’index de base 1 spécifié. |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | Récupère le LCID pour un index de langue audio spécifié.                                         |
| [getLanguageName](controls-getlanguagename.md)                         | Récupère le nom de la langue audio avec le LCID spécifié.                                |
| [suivant](controls-next.md)                                               | Définit l’élément actuel à l’élément suivant dans la sélection.                                          |
| [pause](controls-pause.md)                                             | Suspend la diffusion de l’élément multimédia.                                                            |
| [répétition](controls-play.md)                                               | Entraîne le démarrage de la diffusion de l’élément multimédia.                                                          |
| [playItem](controls-playitem.md)                                       | Entraîne le démarrage de la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.                |
| [previous](controls-previous.md)                                       | Définit l’élément actuel à l’élément précédent dans la sélection.                                      |
| [première](controls-step.md)                                               | Entraîne le blocage de la lecture de l’élément multimédia vidéo actuel sur le frame suivant.                        |
| [stop](controls-stop.md)                                               | Arrête la diffusion de l’élément multimédia.                                                             |



 

L’objet **Controls** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                        |
|-----------------------------|---------------------------------|
| [Lecteur](player-object.md) | [commandes](player-controls.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





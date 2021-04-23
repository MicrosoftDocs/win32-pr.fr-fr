---
description: Le jeu de propriétés de modification du taux active les filtres de source/d’analyseur MPEG-2 pour modifier la vitesse de lecture. Les décodeurs MPEG-2 doivent prendre en charge ce jeu de propriétés. Le navigateur DVD et le moteur de mémoire tampon de flux utilisent tous deux le jeu de propriétés pour contrôler les taux de lecture.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Jeu de propriétés de modification du taux (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb222f8a2fe388d8ea582448d2ba5aa6c9d7e80
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909607"
---
# <a name="rate-change-property-set"></a>Définition de la propriété change rate

Le jeu de propriétés de modification du taux active les filtres de source/d’analyseur MPEG-2 pour modifier la vitesse de lecture. Les décodeurs MPEG-2 doivent prendre en charge ce jeu de propriétés. Le navigateur DVD et le moteur de mémoire tampon de flux utilisent tous deux le jeu de propriétés pour contrôler les taux de lecture.



| Étiquette | Valeur |
|-------------------|-------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange |



 



| ID de propriété                                                                   | Description                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_Taux am \_ CorrectTS**](am-rate-correctts-property.md)                     | Informe le décodeur que le navigateur définit le datage correct.             |
| \_Taux am \_ ExactRateChange                                                     | Obsolète.                                                                              |
| [**\_Taux am \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Interroge le décodeur pour le débit de données maximal du décodeur.                               |
| [**\_Taux am \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Interroge le décodeur pour la fréquence d’images entières maximale du décodeur.                         |
| [**\_Taux am \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Interroge le décodeur pour l’heure de début du segment de taux qui a été défini en dernier. |
| [**\_Taux am \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Envoie une modification de taux au décodeur.                                                    |
| \_Étape am rate \_                                                                | Obsolète. Consultez [jeu de propriétés d’exécution de frames](frame-stepping-property-set.md).          |
| [**\_Taux am \_ UseRateVersion**](am-rate-userateversion-property.md)           | Spécifie la version du mécanisme de modification du taux à utiliser.                           |



 

## <a name="remarks"></a>Remarques

Dans le contexte de ce jeu de propriétés, rate mesure le taux auquel les horodatages avancent par rapport à l’horloge de référence. Évaluer l’inverse de la vitesse de lecture. Par exemple, si la vitesse de lecture est 2x, les horodatages doivent augmenter à 1/2 le taux normal. Cela se traduit par une vitesse de lecture plus rapide, car les échantillons sont rendus antérieurs à la normale.

Les exemples sont envoyés au décodeur avec un horodatage égal à l’heure de présentation au tarif 1x. Le décodeur doit mettre à l’échelle les horodatages sur les échantillons de sortie à l’heure de présentation correcte pour le taux actuel. Par exemple, si le taux est 1/2 (ce qui signifie que la vitesse de lecture est 2x), le décodeur doit mettre à l’échelle les horodatages de 1/2. En règle générale, seules les images ont des horodatages. Le décodeur doit interpoler les horodatages pour les images B et P. Notez que pendant la lecture inversée, les horodatages continuent d’augmenter : les horodatages ne sont jamais retournés en arrière.

Deux versions du jeu de propriétés change rate sont définies, version 1,0 et version 1,1. Le comportement par défaut est donné par la version 1,0. Les fournisseurs de décodeur sont encouragés à prendre en charge la version 1,1, car il fournit une expérience de lecture plus lisse. Le navigateur DVD utilise actuellement la version 1,0. Le moteur de mémoire tampon de flux utilise la version 1,1.

### <a name="rate-change-version-10"></a>Taux de modification de la vitesse 1,0

La version 1,0 de la définition de la propriété change rate définit le comportement par défaut pour les décodeurs MPEG-2.

Le filtre source signale un changement de taux en définissant la propriété [**\_ \_ SimpleRateChange rate am**](am-rate-simpleratechange-property.md) . Les données de cette propriété sont le nouveau taux, plus l’heure de début de l’échantillon d’entrée lorsque le tarif prend effet. Le décodeur gère une file d’attente de modifications de taux en attente, triées par heure de début.

Avant que le navigateur DVD ne passe à une vitesse non-1x, il remet tous les échantillons en attente, définit temporairement le taux sur 1,0 et vide le graphique. Ensuite, il définit le nouveau taux. Toutes les modifications de taux sont planifiées pour la fin du VOBU actuel (unité d’objet vidéo). Notez que le vidage du graphique réinitialise l’heure de la présentation à zéro.

Le navigateur DVD fonctionne en *mode Smooth* ou en *mode d’analyse*. En mode Smooth, il envoie chaque frame au décodeur, y compris les images B et P. Le navigateur DVD utilise le mode Smooth chaque fois que la vitesse de lecture est supérieure à zéro, mais inférieure à la vitesse de données de réexécution réussis du décodeur. Si la vitesse de lecture est inférieure à zéro (lecture inversée) ou dépasse la vitesse de transmission maximale du décodeur, le navigateur DVD utilise le mode d’analyse, où il envoie uniquement les frames I au décodeur. À des vitesses très élevées, il peut ignorer certaines images. par exemple, elle peut être envoyée toutes les autres images.

Par défaut, le navigateur DVD désactive le flux audio pour des vitesses autres que 1,0. Vous pouvez modifier cela en appelant [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) avec l' \_ indicateur DVD AudioDuringFFwdRew.

### <a name="rate-change-version-11"></a>Taux de modification de la vitesse 1,1

La version 1,1 de la définition de la propriété change rate suit les mêmes principes de base que la version 1,0, avec les différences suivantes :

-   Le filtre source indique au décodeur d’utiliser la version 1,1 en définissant la propriété [**\_ \_ UseRateVersion rate am**](am-rate-userateversion-property.md) . Dans le cas contraire, le décodeur doit utiliser le comportement de la version 1,0.
-   Le filtre source n’efface pas le graphique entre les changements de taux. Par conséquent, les horodatages augmentent de manière monotone entre les limites de changement de taux, au lieu de réinitialiser à zéro.
-   Au lieu de mettre en file d’attente un changement de taux pour un temps de référence particulier, le filtre source peut spécifier qu’une modification du taux s’applique à l' *exemple le plus direct* du décodeur, défini comme exemple au début de la file d’attente sortante du décodeur. Pour ce faire, le filtre source utilise la [**propriété \_ \_ SimpleRateChange am rate**](am-rate-simpleratechange-property.md) , mais affecte la valeur-1 à l’heure de début.
-   Le filtre source peut interroger le décodeur pour l’heure de début du changement de taux mis en file d’attente le plus récemment. Elle utilise la [**propriété \_ \_ QueryLastRateSegPTS am rate**](am-rate-querylastratesegpts-property.md) à cet effet.
-   Le filtre source ne supprime pas les exemples. Si le taux dépasse le débit de données maximal du décodeur, le décodeur doit supprimer les frames si nécessaire.
-   Le filtre source n’active pas le silence du flux audio, quelle que soit la vitesse de transmission maximale des données du décodeur audio. Le décodeur audio peut supprimer des échantillons si la vitesse de lecture dépasse la vitesse maximale du décodeur. Toutefois, il doit toujours conserver la file d’attente des changements de taux planifiés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 





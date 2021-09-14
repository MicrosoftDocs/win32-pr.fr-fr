---
description: Contrôles de volume Audio-Tapered
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Contrôles de volume Audio-Tapered
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115081"
---
# <a name="audio-tapered-volume-controls"></a>Contrôles de volume Audio-Tapered

L’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) gère les contrôles de volume dont l’audio est conique. ces contrôles sont bien adaptés à Windows applications qui affichent des curseurs de volume. Pour un curseur de volume qui est lié à un contrôle de volume à cônes audio, chaque modification de la position du curseur produit une modification de la valeur sonore perçue qui est proportionnelle à la distance parcourue par le curseur. Pour une distance de déplacement particulière, la quantité d’augmentation ou de diminution du volume perçu est approximativement la même, que le déplacement du curseur se produise ou non dans la partie inférieure, supérieure ou centrale de la plage de déplacement du curseur. Le bruit perçu varie approximativement de manière linéaire avec le logarithme de la puissance du signal audio.

Le terme « *cône* » à l’origine faisait appel à la forme conique de l’élément résistif dans un potentiomètre utilisé comme contrôle du volume dans un appareil électronique audio. Un élément résistif à cônes audio est le plus large à la position du volume zéro et le plus étroit à la position du volume maximal. Le potentiomètre contrôle le niveau de tension du signal audio que l’appareil lit dans ses haut-parleurs. Le dépouillement est conçu pour produire une relation linéaire approximative entre la position de l’essuie-glace et le bruit perçu aux orateurs. La relation entre la position de l’essuie-glace et la tension aux haut-parleurs est non linéaire.

En revanche, un élément résistif avec un cône linéaire a une largeur uniforme sur la plage de mouvement de l’essuie-glace du potentiomètre. Par conséquent, la tension aux haut-parleurs varie de manière linéaire avec la position de l’essuie-glace. La relation entre la position de l’essuie-glace et le bruit est non linéaire.

de même, une Windows application qui affiche un curseur de volume définit une relation entre la position du curseur et le niveau du signal de sortie aux haut-parleurs. La relation peut, en fait, être linéaire ou conique.

Le diagramme suivant montre le mappage de la position du curseur sur la tension de sortie et le bruit perçu pour un contrôle de volume à cône linéaire.

![diagramme de sortie pour un contrôle de volume linéaire conique](images/taper1.jpg)

Sur le côté gauche du diagramme précédent, le niveau de tension de sortie du convertisseur audio numérique-analogique (DAC) augmente de façon linéaire à mesure que le curseur de volume passe de sa position minimale (étiquetée min) à sa position maximale (étiquetée max). L’étiquette V<sub>FS</sub> sur l’axe vertical représente la tension de sortie DAC à l’échelle complète.

Toutefois, le bruit perçu varie approximativement comme le logarithme de la puissance du signal audio, comme indiqué sur le côté droit du diagramme précédent. Ainsi, le déplacement du curseur sur un intervalle proche de la valeur minimale entraîne une modification relativement importante du volume perçu, mais le déplacement du curseur sur un intervalle de la même largeur près du paramètre maximal entraîne une modification relativement faible du volume perçu.

Sur le côté droit du diagramme précédent, le niveau sonore de l’axe vertical est mesuré en décibels (dB) par rapport au paramètre d’alimentation à pleine échelle (à partir de 0 décibels). La courbe de bruit croise l’axe vertical à moins l’infini, mais seule la partie de la courbe comprise entre 0 décibels et-96 décibels apparaît dans le diagramme. La décision d’afficher uniquement cette partie de la courbe est quelque peu arbitraire, mais-96 décibels représente une puissance au niveau de sortie le plus proche d’une DAC 16 bits par rapport à la puissance à grande échelle. Cette valeur est calculée comme 20<sup>.</sup> log ₁ ₀ (1/65535).

Étant donné que les petites modifications apportées à la position du curseur près du paramètre minimal dans le diagramme précédent entraînent de grandes modifications en intensité, l’utilisateur peut trouver le volume difficile à contrôler sur cette région. Des mouvements de curseur relativement petits peuvent pousser le volume au-dessus ou au-dessous du niveau souhaité. Un contrôle de volume amélioré fournit une relation plus linéaire entre la position du curseur et le bruit.

Le diagramme suivant montre le mappage de la position du curseur sur la tension de sortie et le bruit perçu pour un contrôle de volume à cônes audio.

![diagramme de sortie pour le contrôle du volume à cônes audio](images/taper2.jpg)

Comme indiqué sur le côté droit du diagramme précédent, le bruit perçu varie approximativement de manière linéaire avec les modifications apportées à la position du curseur. Pour que cela se produise, la tension de la DAC doit varier de manière linéaire avec la position, comme indiqué sur le côté gauche du diagramme. La courbe approche asymptotiquement de 0 volts lorsque le curseur se déplace vers la gauche à partir du paramètre maximal. La tension à la position de curseur minimale est très petite, mais elle peut ne pas être exactement égale à zéro.

Les méthodes suivantes de l’interface **IAudioEndpointVolume** utilisent des paramètres de volume mesurés en décibels :

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Ces méthodes produisent une relation linéaire approximative entre les paramètres de volume et les intensités perçues. La plage de volumes, en décibels, des contrôles de volume gérés par ces méthodes dépend du périphérique de point de terminaison audio. Pour déterminer la plage de volumes pour un appareil particulier, appelez la méthode [**IAudioEndpointVolume :: GetVolumeRange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) .

En revanche, les paramètres de volume pour les méthodes suivantes dans l’interface **IAudioEndpointVolume** suivent une courbe conique plus délicate sur la plage de volumes :

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

dans Windows Vista, ces méthodes utilisent une courbe intermédiaire entre la courbe audio-conique indiquée dans le diagramme précédent et une courbe à cône linéaire. Notez que la forme de la courbe peut changer dans les versions ultérieures de Windows. Les quatre premières méthodes de la liste précédente expriment les niveaux de volume comme valeurs normalisées dans la plage comprise entre 0,0 (volume minimum) et 1,0 (volume maximal). Pour les deux dernières méthodes de la liste, appelez la méthode [**IAudioEndpointVolume :: GetVolumeStepInfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) pour obtenir le nombre d’étapes dans la plage de volumes.

Les interfaces suivantes utilisent des courbes linéaires à cônes pour leurs paramètres de volume :

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Pour plus d’informations sur ces interfaces, consultez [contrôles du volume de session](session-volume-controls.md). pour plus d’informations sur les plages de volumes et les niveaux de volume par défaut dans les différentes versions de Windows, consultez [Paramètres de volume Audio par défaut](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de volume](volume-controls.md)
</dt> </dl>

 

 

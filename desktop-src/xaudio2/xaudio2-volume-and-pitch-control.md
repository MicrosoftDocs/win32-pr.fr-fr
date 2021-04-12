---
description: Cette rubrique décrit le contrôle du volume et du tangage XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Contrôle du volume et du tangage XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203787"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Contrôle du volume et du tangage XAudio2

Cette rubrique décrit le contrôle du volume et du tangage XAudio2.

## <a name="volume-control"></a>Contrôle du volume

Les niveaux de volume sont exprimés sous la forme de multiplicateurs d’amplitude à virgule flottante entre-XAUDIO2 \_ Max \_ volume \_ Level et XAUDIO2 \_ Max \_ volume \_ Level (-224 à 224), avec un gain maximal de 144,5 dB. Un volume de 1,0 signifie qu’il n’y a pas d’atténuation ou de gain ; 0 signifie un silence ; les niveaux négatifs peuvent être utilisés pour inverser la phase du son. Deux fonctions inline sont fournies dans XAudio2. h pour effectuer une conversion entre les unités de volume : [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) et [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

Vous pouvez appliquer un niveau de volume à l’audio à plusieurs points au fur et à mesure qu’il traverse le graphique XAudio2 :

-   Tous les types de voix appliquent un niveau de volume global à leur entrée, qu’ils contrôlent à l’aide de la méthode [**IXAudio2Voice :: setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) . Dans les voix de mixage secondaire et de mastérisation, le niveau de volume global est appliqué juste avant le filtre intégré et la chaîne d’effet de la voix. Dans les voix source, le niveau de volume global est appliqué après le filtre intégré et la chaîne d’effet de la voix.
-   Les voix appliquent un niveau de volume par canal à leur sortie, qu’ils contrôlent à l’aide de la méthode [**IXAudio2Voice :: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) . Le niveau de volume par canal est appliqué juste après la conversion du taux d’échantillonnage final de la voix et avant d’être envoyé à d’autres voix.
-   Chaque connexion entre une voix et une autre a une table de niveaux utilisée pour envoyer l’audio de chaque canal source à chaque canal cible, qui est contrôlée à l’aide de la méthode [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .

Tous les volumes globaux et les volumes de canaux sont par défaut de 1,0. Toutes les matrices au niveau de l’envoi ont par défaut des valeurs appropriées qui préservent le positionnement de la puissance et du canal des signaux aussi précisément que possible. Pour plus d’informations, consultez la vue d’ensemble du [mappage de canal par défaut XAudio2](xaudio2-default-channel-mapping.md) .

> [!Note]  
> XAudio2 ajuste automatiquement les niveaux de volume en fonction des paramètres de haut-parleur de l’utilisateur pour conserver un niveau de volume cohérent entre les configurations. Si les paramètres de l’utilisateur ne correspondent pas à leur configuration physique, le volume est trop fort ou trop faible comparé à un système avec des paramètres précis. Par exemple, un système configuré pour des enceintes de son surround 5,1 qui n’a que deux haut-parleurs connectés est trop léger. XAudio2 ne peut pas détecter si les paramètres de haut-parleur de l’utilisateur correspondent correctement à leur configuration physique.

 

## <a name="pitch-control"></a>Contrôle de la hauteur

Les tonalités sont exprimées en tant que taux d’entrée/taux de débit de sortie compris entre 1/1024 et 1024/1, inclus. Un ratio de 1/1024 réduit le pas de 10 octaves, tandis qu’un ratio de 1 024/1 l’élève de 10 octaves. Vous pouvez uniquement utiliser la méthode [**IXAudio2SourceVoice :: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) pour appliquer des ajustements de pas aux voix source, et uniquement si elles n’ont pas été créées avec l’indicateur de \_ vocal XAUDIO2 \_ . Le rapport de fréquence par défaut est 1/1 : autrement dit, aucune modification de la tonalité. Deux fonctions inline sont fournies dans XAudio2. h pour effectuer une conversion entre les coefficients de fréquence et les demi-tons : [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) et [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle du volume et de la hauteur](volume-and-pitch-control.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Comment : modifier la tonalité des voix](how-to--change-voice-pitch.md)
</dt> <dt>

[Comment : modifier le volume vocal](how-to--change-voice-volume.md)
</dt> </dl>

 

 

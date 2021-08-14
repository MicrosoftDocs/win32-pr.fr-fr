---
description: X3DAudio est une API utilisée avec XAudio2 pour positionner le son dans l’espace 3D afin de créer l’illusion du son venant d’un point dans l’espace par rapport à la position de l’appareil photo.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Présentation de X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb39239027bf8c7387fbe4cb25b80cef88bb241b74facf0b7bd7ee35c77965b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962548"
---
# <a name="x3daudio-overview"></a>Présentation de X3DAudio

X3DAudio est une API utilisée avec [XAudio2](programming-guide.md) pour positionner le son dans l’espace 3D afin de créer l’illusion du son venant d’un point dans l’espace par rapport à la position de l’appareil photo. En particulier, les titres qui comprendront des scènes en 3D veulent utiliser X3DAudio. Les sons ne nécessitant pas de positionnement 3D, tels que des bandes-son ou des sons ambiants non positionnés, peuvent contourner complètement X3DAudio.

## <a name="listeners-and-emitters"></a>Écouteurs et émetteurs

Pour gérer les sons dans l’espace 3D, X3DAudio utilise les concepts des *écouteurs* et des *émetteurs*. Les écouteurs et les émetteurs représentent la position des sons 3D, ainsi que le point à partir duquel ces sons proviennent.

-   Un écouteur est défini comme un point dans l’espace et une orientation. Il s’agit de la position à laquelle le son est *entendu*. La position et l’orientation de l’écouteur sont généralement les mêmes que la position et l’orientation de l’appareil photo. C’est le cas, qu’un titre utilise une vue en perspective première personne ou tierce personne. La position de l’écouteur est exprimée en coordonnées universelles. Il est important de noter qu’il s’agit de la position de l’écouteur *par rapport* à un émetteur qui détermine le mode de calcul des volumes de haut-parleur final.
-   Un émetteur est défini comme un (ou plusieurs) points dans l’espace à partir duquel un son *provient*. La position de l’émetteur peut être n’importe où dans l’espace 3D. À l’instar d’un écouteur, la position d’un émetteur est exprimée en coordonnées universelles. Il s’agit de la position de l’émetteur *par rapport* à l’écouteur qui détermine la façon dont les volumes de haut-parleur final sont calculés.
-   X3DAudio utilise les coordonnées de la main gauche. Pour une utilisation avec des coordonnées droitiers, les développeurs doivent nier l’élément. z des membres OrientTop, OrientFront, position et Velocity de l' \_ écouteur X3DAUDIO et de l' \_ émetteur X3DAUDIO.

En plus de la position, les écouteurs et les émetteurs peuvent inclure la vélocité. Contrairement à un moteur de rendu 3D, X3DAudio utilise uniquement la vélocité pour calculer les effets Doppler (il n’est pas utilisé pour calculer la position).

Pour plus d’informations sur les écouteurs et les émetteurs, consultez les rubriques de référence sur l' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et la structure de l' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

## <a name="using-x3daudio-with-xaudio2"></a>Utilisation de X3DAudio avec XAudio2

Pour toute interaction entre X3DAudio et XAudio2, utilisez les fonctions X3DAudio suivantes.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Appelez la fonction [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) pour initialiser X3DAudio. En règle générale, il vous suffit d’appeler **X3DAudioInitialize** une fois pendant la durée de vie d’un jeu, sauf si la configuration de l’orateur est modifiée.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Après l’initialisation de X3DAudio, vous pouvez déterminer le volume et d’autres valeurs pour un son donné en passant l’émetteur du son et l’écouteur à la fonction [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) . Les valeurs calculées par **X3DAudioCalculate** peuvent ensuite être appliquées aux voix de XAudio2 ou aux effets appropriés pour les indicateurs passés à la fonction. Vous pouvez appliquer des valeurs de volume et de tonalité calculées par X3DAudio à une voix avec les méthodes [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) et [**IXAudio2SourceVoice :: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) . D’autres valeurs calculées par X3DAudio doivent être appliquées à un [**effet de réverbération**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) à l’aide de la méthode [**IXAudio2Voice :: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) .

Pour obtenir un exemple pas à pas d’utilisation de X3DAudio avec XAudio2, consultez [Comment : intégrer X3DAudio à xaudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 

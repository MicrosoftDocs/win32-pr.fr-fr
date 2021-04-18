---
description: 'Il existe trois types d’objets vocaux XAudio2 : les voix source, de mixage secondaire et de mastérisation.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voix XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520157"
---
# <a name="xaudio2-voices"></a>Voix XAudio2

Il existe trois types d’objets vocaux XAudio2 : les voix *source*, de *mixage secondaire* et de *mastérisation* . Les voix source opèrent sur les données audio fournies par le client. Les voix source et sous-mixées envoient leur sortie vers une ou plusieurs voix sous-mixées ou de matriçage. Les voix sous-mixées et de matriçage mixent les signaux provenant de toutes les voix qui les alimentent et opèrent sur le résultat. Les voix de matriçage écrivent des données audio sur un périphérique audio.

## <a name="actions-performed-by-all-voices"></a>Actions effectuées par toutes les voix

Toutes les voix effectuent les actions suivantes dans l’ordre audio qui les traverse.

1.  Réglage global du volume, affectant tous les canaux audio. Consultez [**IXAudio2Voice :: setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Chaîne facultative spécifiée par le client d’un ou de plusieurs effets DSP, comme le verbe intégré ou l’effet utilisateur défini par l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) . Consultez [effets audio XAudio2](xaudio2-audio-effects.md).
3.  Réglage du volume de sortie par canal. Consultez [**IXAudio2Voice :: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Mélange de matrices distincts à chacune des voix de destination ou à l’appareil de sortie audio pour la maîtrise des voix. Cette combinaison modifie le nombre de canaux dans l’audio, si nécessaire.

## <a name="source-voices"></a>Voix source

Utilisez les voix source pour envoyer des données audio dans le pipeline de traitement XAudio2. Il s’agit des points d’entrée dans le [graphique audio XAudio2](xaudio2-audio-graph.md). Vous devez envoyer des données vocales à une voix de mastérisation pour être entendues, soit directement, soit par le biais de voix de mixage secondaire intermédiaires.

En plus des actions effectuées par toutes les voix, les voix source effectuent les actions suivantes.

-   Si nécessaire, un décodeur s’exécute en premier pour convertir les données sources encodées en PCM (Pulse Code Modulation).
-   Une conversion de taux d’échantillonnage à taux variable (SRC) convertit les données audio sources de la voix en taux d’échantillonnage attendu par ses voix de destination, si nécessaire, et prend également en charge les changements de pas dynamique.
-   Un filtre de variable d’État facultatif peut être utilisé pour colorer le son de différentes façons. Consultez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Un filtre facultatif peut être appliqué aux sorties de la voix. Consultez [**IXAudio2Voice :: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Voix de mixage secondaire

Une voix de mixage secondaire est principalement utilisée pour améliorer les performances et le traitement des effets. Vous ne pouvez pas envoyer directement des tampons de données à des voix de mixage secondaire. Il ne sera pas audible, sauf si vous le soumettez à une voix de mastérisation. Vous pouvez utiliser une voix de mixage secondaire pour vous assurer qu’un ensemble particulier de données vocales est converti au même format et qu’une chaîne d’effet particulière est traitée sur le résultat collectif.

En plus des actions effectuées par toutes les voix, les voix de mixage secondaire effectuent les actions suivantes.

-   Un SRC à débit fixe s’exécute sur la sortie de la voix, si nécessaire, pour convertir l’audio en taux d’échantillonnage attendu par ses voix de destination.
-   Un filtre de variable d’État facultatif peut être utilisé pour colorer le son de différentes façons. Consultez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Un filtre facultatif peut être appliqué aux sorties de la voix. Consultez [**IXAudio2Voice :: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Mastérisation des voix

Utilisez une voix de mastérisation pour représenter l’appareil de sortie audio. Vous ne pouvez pas envoyer de tampons de données directement à des voix de mastérisation, mais les données soumises à d’autres types de voix doivent être envoyées à une voix de mastérisation.

En plus des actions effectuées par toutes les voix, les voix de mastérisation effectuent les actions suivantes.

-   Si vous créez la voix de mastérisation avec une valeur *InputSampleRate* explicite qui n’est pas prise en charge par le périphérique audio, un SRC à débit fixe est utilisé pour convertir le taux d’échantillonnage le plus proche pris en charge par l’appareil.
-   Découpez la sortie audio finale, si elle est requise par le périphérique de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Voix](voices.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 

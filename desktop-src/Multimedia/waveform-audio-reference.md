---
title: Référence sur l’audio Waveform
description: Cette section répertorie les fonctions, structures et messages associés à la forme d’onde audio, qui sont documentées sous référence multimédia. Ces éléments sont regroupés comme suit.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows multimédia, référence audio de forme d’onde
- multimédia, référence audio de forme d’onde
- audio multimédia, référence de forme d’onde
- audio, référence de forme d’onde
- Windows multimédia, audio waveform
- multimédia, audio Waveform
- audio multimédia, forme d’onde
- audio, forme d’onde
- onde audio, référence
- Référence audio Waveform, à propos de
- référence pour wavefore audio, à propos de
- Référence audio Waveform, appareils auxiliaires
- référence pour wavefore audio, appareils auxiliaires
- Référence audio Waveform, lecture
- référence pour l’audio wavefore, lecture
- Référence audio Waveform, Erreurs
- référence pour wavefore audio, Erreurs
- Référence audio Waveform, ouverture
- référence pour l’audio wavefore, ouverture
- Référence audio Waveform, fermeture
- référence pour l’audio wavefore, fermeture
- Référence audio Waveform, inclinaison
- référence pour l’audio wavefore, la tonalité
- Référence audio Waveform, volume
- référence pour wavefore audio, volume
- Référence audio Waveform, messages
- informations de référence sur l’audio wavefore, messages
- Référence audio de forme d’onde, position actuelle
- référence pour l’audio wavefore, position actuelle
- Référence audio Waveform, enregistrement
- informations de référence sur l’audio wavefore, enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd83f843de130d247749acfc87a67c60948871bb8cd878f9aa180fcd385fb13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687419"
---
# <a name="waveform-audio-reference"></a>Référence sur l’audio Waveform

Cette section répertorie les fonctions, structures et messages associés à la forme d’onde audio, qui sont documentées sous [référence multimédia](multimedia-reference.md). Ces éléments sont regroupés comme suit.

## <a name="auxiliary-devices"></a>Périphériques auxiliaires

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Lecture facile

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Ouverture et fermeture

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**\_fermeture de Wim de mm \_**](mm-wim-close.md)
-   [**fichier \_ Wim \_ Open**](mm-wim-open.md)
-   [**MM \_ WOM \_ Fermer**](mm-wom-close.md)
-   [**MM \_ WOM \_ ouverts**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**fermeture de WIM \_**](wim-close.md)
-   [**\_ouvrir Wim**](wim-open.md)
-   [**WOM \_ Fermer**](wom-close.md)
-   [**WOM \_ ouvrir**](wom-open.md)

## <a name="pitch"></a>Inclinaison

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Vitesse de lecture

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Progression de la lecture

-   [**MM \_ WOM \_ terminé**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ terminé**](wom-done.md)

## <a name="playing"></a>Lecture en cours

-   [**MM \_ WOM \_ terminé**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ terminé**](wom-done.md)

## <a name="querying-a-device"></a>Interrogation d’un appareil

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Enregistrement

-   [**\_données Wim \_ mm**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**\_données Wim**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Récupération des identificateurs d’appareil

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Récupération de la position actuelle

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Envoi de messages personnalisés

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volume

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sons Waveform](waveform-audio.md)
</dt> </dl>

 

 
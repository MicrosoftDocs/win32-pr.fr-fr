---
title: Informations de référence MIDI
description: Informations de référence MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows multimédia, MIDI (Musical Instrument Digital Interface)
- multimédia, MIDI (Musical Instrument Digital Interface)
- audio multimédia, MIDI (Musical Instrument Digital Interface)
- audio, MIDI (Musical Instrument Digital Interface)
- Windows multimédia, référence MIDI
- multimédia, référence MIDI
- audio multimédia, référence MIDI
- audio, référence MIDI
- Informations de référence sur l’interface MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), référence
- référence pour MIDI, à propos de
- Référence MIDI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364344"
---
# <a name="midi-reference"></a>Informations de référence MIDI

Cette section décrit les fonctions, les macros, les messages et les structures associés à l’interface MIDI (Musical Instrument Digital Interface). Ces éléments sont regroupés comme suit.

## <a name="allocating-and-managing-buffers"></a>Allocation et gestion des mémoires tampons

-   [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Fonctions de rappel

-   [**MidiInProc**](/previous-versions//dd798460(v=vs.85))
-   [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Fonctionnalités de l’appareil

-   [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**midiInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**midiOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**MIDISTRMBUFFVER**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Erreur lors du traitement

-   [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**MIM \_ Erreurs**](mim-error.md)
-   [**MIM \_ LONGERROR**](mim-longerror.md)
-   [**MM \_ MIM \_ erreur**](mm-mim-error.md)
-   [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Gestion des Flux MIDI

-   [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Ouverture et fermeture des appareils

-   [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**MIM \_ PLUS**](mim-close.md)
-   [**MIM \_ AFFICHER**](mim-open.md)
-   [**MM \_ MIM \_ fermer**](mm-mim-close.md)
-   [**MM \_ MIM \_ ouverts**](mm-mim-open.md)
-   [**\_fermeture MOM de mm \_**](mm-mom-close.md)
-   [**\_ouverture de MOM mm \_**](mm-mom-open.md)
-   [**\_fermeture MOM**](mom-close.md)
-   [**MOM \_ ouvert**](mom-open.md)

## <a name="output-devices"></a>Périphériques de sortie

-   [Tableau de la matrice](keyarray.md)
-   [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>La diffusion d’un message ou de messages

-   [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**\_eventType MEVT**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM \_ MOM \_ terminé**](mm-mom-done.md)
-   [**MM \_ \_ POSITIONCB MOM**](mm-mom-positioncb.md)
-   [**MOM \_ terminé**](mom-done.md)
-   [**\_POSITIONCB MOM**](mom-positioncb.md)

## <a name="recording"></a>Enregistrement

-   [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**midiDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**MIDIPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**MIDIPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**MIM \_ MÉTADONNÉE**](mim-data.md)
-   [**MIM \_ LONGDATA**](mim-longdata.md)
-   [**MIM \_ MOREDATA**](mim-moredata.md)
-   [**MM \_ MIM \_ données**](mm-mim-data.md)
-   [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Envoi de messages à des appareils

-   [**midiInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midiOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interface MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 
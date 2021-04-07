---
title: À propos de MIDI
description: À propos de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimédia Windows, MIDI (Musical Instrument Digital Interface)
- multimédia, MIDI (Musical Instrument Digital Interface)
- audio multimédia, MIDI (Musical Instrument Digital Interface)
- audio, MIDI (Musical Instrument Digital Interface)
- Interface MIDI (Musical Instrument Digital Interface), à propos de
- MIDI (Musical Instrument Digital Interface), à propos de
- Interface MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), services MIDI
- MIDI (Musical Instrument Digital Interface), services MIDI
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- mémoires tampons de flux, à propos de
- Services MIDI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672150"
---
# <a name="about-midi"></a>À propos de MIDI

L’interface de programmation d’applications (API) Microsoft Win32 fournit les méthodes suivantes pour que les applications fonctionnent avec des données MIDI :

-   L’interface MCI (Media Control Interface). Bien que la façon la plus simple de lire un fichier MIDI consiste à utiliser la classe de fenêtre MCIWnd, vous pouvez également utiliser des commandes MCI pour créer une interface personnalisée sur un appareil MIDI. Pour plus d’informations sur la classe de fenêtre MCIWnd, consultez [classe de fenêtre MCIWnd](mciwnd-window-class.md). Pour plus d’informations sur MCI, consultez [MCI](mci.md)ou [MCI (Media Control Interface)](media-control-interface--mci.md).
-   [Mémoires tampons de flux](stream-buffers.md). Ce format permet à une application de manipuler des mémoires tampons de données MIDI horodatées pour la lecture. Les mémoires tampons de flux sont utiles pour les applications qui requièrent un contrôle plus précis de la sortie que les offres MCI.
-   [Services midi](midi-services.md). Les applications qui ont besoin d’un contrôle plus précis des données MIDI utilisent généralement ces services de bas niveau.

Les rubriques suivantes décrivent chacune de ces méthodes et fournissent une vue d’ensemble du mappeur MIDI.

-   [Le Mappeur MIDI](the-midi-mapper.md)
-   [MCI (Media Control Interface)](media-control-interface--mci.md)
-   [Mémoires tampons de flux](stream-buffers.md)
-   [Services MIDI](midi-services.md)
-   [Jeux de fichiers MIDI en train de fonctionner](playing-midi-files.md)
-   [Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
-   [Traitement des données MIDI à partir de deux sources MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Création de fichiers MIDI](creating-midi-files.md)

 

 





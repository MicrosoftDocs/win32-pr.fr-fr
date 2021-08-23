---
title: À propos de MIDI
description: À propos de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimédia, MIDI (Musical Instrument Digital Interface)
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
ms.openlocfilehash: ad1ce20164c42342c52defd27e7f3ccdfb0a44ec9a4e0a6679c1b190270fc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526689"
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

 

 





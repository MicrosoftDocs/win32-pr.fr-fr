---
title: MCI (Media Control Interface)
description: MCI (Media Control Interface)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows multimédia, MCI (Media Control Interface)
- multimédia, MCI (Media Control Interface)
- audio multimédia, MCI (Media Control Interface)
- audio, MCI (Media Control Interface)
- Interface MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI Sequencer
- MCI (Media Control Interface), MIDI Sequencer
- Séquenceur MIDI MCI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011761"
---
# <a name="media-control-interface-mci"></a>MCI (Media Control Interface)

MCI MIDI Sequencer est le composant système MCI qui lit les fichiers MIDI. Les applications peuvent lire des fichiers MIDI facilement à l’aide de MCI, mais MCI impose les restrictions suivantes sur les fonctionnalités MIDI :

-   MCI prend en charge la sortie MIDI uniquement.
-   MCI n’autorise pas la synchronisation étroite entre les événements MIDI et les autres événements en temps réel (tels que la vidéo).

Si vous avez besoin d’une synchronisation MIDI exacte, vous devez utiliser les mémoires tampons de flux ou les services MIDI. Si vous avez besoin de fonctionnalités d’entrée MIDI, vous devez utiliser les services MIDI.

Le séquenceur MIDI MCI lit les fichiers MIDI standard et les fichiers MIDI RIFF (Resource Interchange File Format), appelés fichiers RMID. Les fichiers MIDI standard sont conformes à la spécification [1,0 des fichiers MIDI standard](creating-midi-files.md) . Étant donné que les fichiers RMID sont des fichiers MIDI standard avec un en-tête RIFF, les informations sur les fichiers MIDI standard s’appliquent également aux fichiers RMID. Pour plus d’informations sur les fichiers RIFF, consultez [services de format de fichier](resource-interchange-file-format-services.md)de l’échange de ressources.

Bien qu’il existe actuellement trois types de fichiers MIDI standard, le séquenceur MCI ne lit que deux d’entre eux : le format 0 et le format 1 fichiers MIDI.

Pour plus d’informations sur le contrôle des appareils multimédias (y compris les séquenceurs) à l’aide des commandes MCI, consultez [MCI](mci.md).

 

 





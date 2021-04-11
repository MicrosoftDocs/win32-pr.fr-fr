---
title: Gestion de l’enregistrement Waveform-Audio
description: Gestion de l’enregistrement Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio Wave, enregistrement
- Waveform-interface audio, enregistrement
- enregistrement de la forme d’onde audio, à propos de
- WAVEHDR, structure
- waveInAddBuffer fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314772"
---
# <a name="managing-waveform-audio-recording"></a>Gestion de l’enregistrement Waveform-Audio

Après avoir ouvert un périphérique d’entrée Waveform-Audio, vous pouvez commencer à enregistrer des données Waveform-Audio. Les données Waveform-Audio sont enregistrées dans des mémoires tampons fournies par l’application spécifiées par une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) . Ces blocs de données doivent être préparés avant d’être utilisés ; Pour plus d’informations, consultez [blocs de données audio](audio-data-blocks.md).

Windows fournit les fonctions suivantes pour gérer l’enregistrement Waveform-Audio.



| Fonction                                   | Description                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Envoie une mémoire tampon au pilote de périphérique pour qu’elle puisse être remplie avec des données Waveform-audio enregistrées. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Arrête l’enregistrement Waveform-Audio et marque toutes les mémoires tampons en attente comme terminées.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Démarre l’enregistrement Waveform-Audio.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Arrête l’enregistrement Waveform-Audio.                                                            |



 

Utilisez la fonction [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) pour envoyer des tampons au pilote de périphérique. Étant donné que les tampons sont remplis avec des données Waveform-audio enregistrées, l’application est avertie par un message de fenêtre, un message de rappel, un message de thread ou un événement, en fonction de l’indicateur spécifié lors de l’ouverture de l’appareil.

Avant de commencer l’enregistrement à l’aide de [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), vous devez envoyer au moins une mémoire tampon au pilote, ou les données entrantes peuvent être perdues.

Avant de fermer l’appareil à l’aide de [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), appelez [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) pour marquer tous les blocs de données en attente comme étant terminés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 
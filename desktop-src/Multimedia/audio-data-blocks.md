---
title: Blocs de données audio
description: Blocs de données audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimédia, blocs de données
- audio, blocs de données
- audio Waveform, blocs de données
- blocs de données audio, à propos de
- WAVEHDR, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940877"
---
# <a name="audio-data-blocks"></a>Blocs de données audio

Les fonctions [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) et [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) requièrent que les applications allouent des blocs de données à transmettre aux pilotes de périphérique à des fins d’enregistrement ou de lecture. Ces deux fonctions utilisent la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour décrire son bloc de données.

Avant d’utiliser l’une de ces fonctions pour passer un bloc de données à un pilote de périphérique, vous devez allouer de la mémoire pour le bloc de données et la structure d’en-tête qui décrit le bloc de données. Les en-têtes peuvent être préparés et déspréparés à l’aide des fonctions suivantes.



| Fonction                                                 | Description                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prépare un bloc de données d’entrée Waveform Audio.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Nettoie la préparation sur un bloc de données d’entrée Waveform Audio.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prépare un bloc de données de sortie Waveform-Audio.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Nettoie la préparation sur un bloc de données de sortie Waveform-Audio. |



 

Avant de passer un bloc de données audio à un pilote de périphérique, vous devez préparer le bloc de données en le transmettant à [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) ou [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader). Lorsque le pilote de périphérique est terminé avec le bloc de données et le retourne, vous devez nettoyer cette préparation en passant le bloc de données à [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) ou [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) avant que toute mémoire allouée puisse être libérée.

Sauf si les données d’entrée et de sortie Waveform-Audio sont suffisamment petites pour être contenues dans un bloc de données unique, les applications doivent fournir continuellement le pilote de périphérique avec des blocs de données jusqu’à la fin de la lecture ou de l’enregistrement.

Même si un bloc de données unique est utilisé, une application doit être en mesure de déterminer à quel moment un pilote de périphérique est terminé avec le bloc de données pour que l’application puisse libérer la mémoire associée au bloc de données et à la structure d’en-tête. Il existe plusieurs façons de déterminer quand un pilote de périphérique est terminé avec un bloc de données :

-   En spécifiant une fonction de rappel pour recevoir un message envoyé par le pilote lorsqu’il se termine par un bloc de données
-   À l’aide d’un rappel d’événement
-   En spécifiant une fenêtre ou un thread pour recevoir un message envoyé par le pilote lorsqu’il se termine avec un bloc de données
-   En interrogeant le \_ bit WHDR Done dans le membre **dwFlags** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) envoyée avec chaque bloc de données

Si une application n’obtient pas de bloc de données au pilote de périphérique si nécessaire, il peut y avoir un décalage audible en lecture ou une perte d’informations enregistrées. Cela nécessite au moins un schéma de double mise en mémoire tampon, en conservant au moins un bloc de données avant le pilote de périphérique.

Les rubriques suivantes décrivent les différentes façons de déterminer quand un pilote de périphérique est terminé avec un bloc de données :

Utilisation d’une fonction de rappel pour traiter des messages de pilote

-   [Utilisation d’une fonction de rappel pour traiter des messages de pilote](using-a-callback-function-to-process-driver-messages.md)
-   [Utilisation d’un rappel d’événement pour traiter des messages de pilote](using-an-callback-to-process-driver-messages.md)
-   [Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote](using-a-window-or-thread-to-process-driver-messages.md)
-   [Gestion des blocs de données par interrogation](managing-data-blocks-by-polling.md)

 

 